### Panel Groups

You can create (collapsible) panel groups easily using the `Bootstrap.PanelHelper`:

-- TABS: panel-grousp-1

-- TAB: php

```php
echo $this->Panel->startGroup();
echo $this->Panel->create('My Panel 1');
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->create('My Panel 2'); // You don't need to close the previous panel!
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->create('My Panel 3');
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->endGroup();
```


-- TAB: Markup

```markup
<div role="tablist" aria-multiselectable="1" id="panelGroup-1" class="panel-group">
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-0">
            <h4 class="panel-title"><a href="#collapse-0" data-toggle="collapse" data-parent="#panelGroup-1" aria-expanded="true" aria-controls="#collapse-0">My Panel 1</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-0" id="collapse-0" class="panel-collapse collapse in">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-1">
            <h4 class="panel-title"><a href="#collapse-1" data-toggle="collapse" data-parent="#panelGroup-1" aria-expanded="false" aria-controls="#collapse-1">My Panel 2</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-1" id="collapse-1" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-2">
            <h4 class="panel-title"><a href="#collapse-2" data-toggle="collapse" data-parent="#panelGroup-1" aria-expanded="false" aria-controls="#collapse-2">My Panel 3</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-2" id="collapse-2" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
</div>
```

-- TAB: Output

<div role="tablist" aria-multiselectable="1" id="panelGroup-1" class="panel-group">
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-0">
            <h4 class="panel-title"><a href="#collapse-0" data-toggle="collapse" data-parent="#panelGroup-1" aria-expanded="true" aria-controls="#collapse-0">My Panel 1</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-0" id="collapse-0" class="panel-collapse collapse in">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-1">
            <h4 class="panel-title"><a href="#collapse-1" data-toggle="collapse" data-parent="#panelGroup-1" aria-expanded="false" aria-controls="#collapse-1">My Panel 2</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-1" id="collapse-1" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-2">
            <h4 class="panel-title"><a href="#collapse-2" data-toggle="collapse" data-parent="#panelGroup-1" aria-expanded="false" aria-controls="#collapse-2">My Panel 3</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-2" id="collapse-2" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
</div>

-- TABS


The `id` of the panel group is automatically generated by default, you can customize it by passing the `id` option to the `startGroup()` method:

```php
echo $this->Panel->startGroup(['id' => 'my-custom-id']);
```

If you do not want the first panel to be open, you can set the `'open' => false` option and then use `'open' => true` when creating a panel:

-- TABS: panel-groups-2

-- TAB: PHP

```php
echo $this->Panel->startGroup(['open' => false]);
echo $this->Panel->create('My Panel 1');
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->create('My Panel 2', ['open' => true]);
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->create('My Panel 3');
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->endGroup();
```

-- TAB: Markup

```markup
<div role="tablist" aria-multiselectable="1" id="panelGroup-3" class="panel-group">
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-3">
            <h4 class="panel-title"><a href="#collapse-3" data-toggle="collapse" data-parent="#panelGroup-3" aria-expanded="false" aria-controls="#collapse-3">My Panel 1</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-3" id="collapse-3" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-4">
            <h4 class="panel-title"><a href="#collapse-4" data-toggle="collapse" data-parent="#panelGroup-3" aria-expanded="true" aria-controls="#collapse-4">My Panel 2</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-4" id="collapse-4" class="panel-collapse collapse in">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-5">
            <h4 class="panel-title"><a href="#collapse-5" data-toggle="collapse" data-parent="#panelGroup-3" aria-expanded="false" aria-controls="#collapse-5">My Panel 3</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-5" id="collapse-5" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
</div>
```

-- TAB: Output

<div role="tablist" aria-multiselectable="1" id="panelGroup-3" class="panel-group">
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-3">
            <h4 class="panel-title"><a href="#collapse-3" data-toggle="collapse" data-parent="#panelGroup-3" aria-expanded="false" aria-controls="#collapse-3">My Panel 1</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-3" id="collapse-3" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-4">
            <h4 class="panel-title"><a href="#collapse-4" data-toggle="collapse" data-parent="#panelGroup-3" aria-expanded="true" aria-controls="#collapse-4">My Panel 2</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-4" id="collapse-4" class="panel-collapse collapse in">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading" role="tab" id="heading-5">
            <h4 class="panel-title"><a href="#collapse-5" data-toggle="collapse" data-parent="#panelGroup-3" aria-expanded="false" aria-controls="#collapse-5">My Panel 3</a></h4>
        </div>
        <div role="tabpanel" aria-labelledby="heading-5" id="collapse-5" class="panel-collapse collapse">
            <div class="panel-body">
                <p>Here I can write my panel content... </p>
            </div>
        </div>
    </div>
</div>

-- TABS

### Non collapsible groups

The panel are collapsible by default, but you can have non collapsible panels if you want:

-- TABS: panel-groups-3

-- TAB: PHP

```php
echo $this->Panel->startGroup(['collapsible' => false]);
echo $this->Panel->create('My Panel 1');
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->create('My Panel 2');
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->create('My Panel 3');
echo '<p>Here I can write my panel content... </p>';
echo $this->Panel->endGroup();
```

-- TAB: Markup

```markup
<div role="tablist" aria-multiselectable="1" id="panelGroup-2" class="panel-group">
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">My Panel 1</h4>
        </div>
        <div class="panel-body">
            <p>Here I can write my panel content... </p>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">My Panel 2</h4>
        </div>
        <div class="panel-body">
            <p>Here I can write my panel content... </p>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">My Panel 3</h4>
        </div>
        <div class="panel-body">
            <p>Here I can write my panel content... </p>
        </div>
    </div>
</div>
```

-- TAB: Output
<div role="tablist" aria-multiselectable="1" id="panelGroup-2" class="panel-group">
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">My Panel 1</h4>
        </div>
        <div class="panel-body">
            <p>Here I can write my panel content... </p>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">My Panel 2</h4>
        </div>
        <div class="panel-body">
            <p>Here I can write my panel content... </p>
        </div>
    </div>
    <div class="panel panel-default">
        <div class="panel-heading">
            <h4 class="panel-title">My Panel 3</h4>
        </div>
        <div class="panel-body">
            <p>Here I can write my panel content... </p>
        </div>
    </div>
</div>

-- TABS