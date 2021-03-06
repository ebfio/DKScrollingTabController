DKScrollingTabController
========================

A Scrolling Tab iOS Control

![](Assets/demo.gif)

# Installation
Add the files in the DKScrollingTabController folder to your project.

# Usage

```  objc
- (id)initWithNibName:(NSString *)nibNameOrNil bundle:(NSBundle *)nibBundleOrNil
{
    self = [super initWithNibName:nibNameOrNil bundle:nibBundleOrNil];
    if (self) {
        // Add controller as a child view controller (standard view controller containment)
        DKScrollingTabController *tabController = [[DKScrollingTabController alloc] init];
        [self addChildViewController:tabController];
        [tabController didMoveToParentViewController:self];
        [self.view addSubview:tabController.view];
        
        // Customize the tab controller (more options in DKScrollingTabController.h or check the demo)
        tabController.view.frame = CGRectMake(0, 20, 320, 40);
        tabController.buttonPadding = 23;
        tabController.selection = @[@"zero", @"one", @"two", @"three", @"four",];
        
        // Set the delegate (conforms to DKScrollingTabControllerDelegate)
        tabController.delegate = self;
    }
    return self;
}


#pragma mark - DKScrollingTabControllerDelegate

- (void)DKScrollingTabController:(DKScrollingTabController *)controller selection:(NSUInteger)selection {
    NSLog(@"Selection controller action button with index=%d",selection);
}

```

# Demo
DKScrollingTabController includes a sample project in the Demo folder.


# Compatibility
- This project uses ARC.
- This project was tested with iOS 6.1 and iOS 7.

# TODO

- Unit tests
- Blur without using `UIToolbar`


# Say Hi
- [github.com/dkhamsing](https://github.com/dkhamsing)
- [twitter.com/dkhamsing](https://twitter.com/dkhamsing)
- [contact](http://dkhamsing.tumblr.com/ask)

# License
DKScrollingTabController is available under the MIT license. See the [LICENSE](LICENSE) file for more info.
