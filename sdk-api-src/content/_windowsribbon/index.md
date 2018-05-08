---
UID: TP:windowsribbon
ms.assetid: 4cd0882b-8e17-315a-8b08-7f07ef01a8d7
ms.author: windowsdriverdev
ms.date: 05/07/18
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: portal
---

# Windows Ribbon Framework



Overview of the Windows Ribbon Framework technology.

To develop Windows Ribbon Framework, you need these headers:

 * [uiribbon.h](..\uiribbon\index.md)

For the programming guide, see [Windows Ribbon Framework](https://review.docs.microsoft.com/en-us/win32-test/windowsribbon).

## Structures

| Title   | Description   |
| ---- |:---- |
| [_UI_EVENTPARAMS structure](..\uiribbon\ns-uiribbon-_ui_eventparams.md) | Contains information about a Ribbon event. |
| [_UI_EVENTPARAMS_COMMAND structure](..\uiribbon\ns-uiribbon-_ui_eventparams_command.md) | Contains information about a Command associated with a event. |

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [UI_COLLECTIONCHANGE enumeration](..\uiribbon\ne-uiribbon-ui_collectionchange.md) | Specifies values that identify the types of changes that can be made to a collection. |
| [UI_COMMANDTYPE enumeration](..\uiribbon\ne-uiribbon-ui_commandtype.md) | Specifies values that identify the type of Command associated with a Ribbon control. |
| [UI_CONTEXTAVAILABILITY enumeration](..\uiribbon\ne-uiribbon-ui_contextavailability.md) | Specifies values that identify the availability of a contextual tab. |
| [UI_CONTROLDOCK enumeration](..\uiribbon\ne-uiribbon-ui_controldock.md) | Specifies values that identify the dock state of the Quick Access Toolbar (QAT). |
| [UI_EVENTLOCATION enumeration](..\uiribbon\ne-uiribbon-ui_eventlocation.md) | Identifies the locations where events associated with a Ribbon control can originate. |
| [UI_EVENTTYPE enumeration](..\uiribbon\ne-uiribbon-ui_eventtype.md) | Identifies the types of events associated with a Ribbon. |
| [UI_EXECUTIONVERB enumeration](..\uiribbon\ne-uiribbon-ui_executionverb.md) | Specifies values that identify the execution IDs that map to actions a user can initiate on a Command. |
| [UI_FONTDELTASIZE enumeration](..\uiribbon\ne-uiribbon-ui_fontdeltasize.md) | Specifies values that identify whether the font size of a highlighted text run should be incremented or decremented. |
| [UI_FONTPROPERTIES enumeration](..\uiribbon\ne-uiribbon-ui_fontproperties.md) | Specifies values that identify the font property state of a FontControl, such as Strikethrough. |
| [UI_FONTUNDERLINE enumeration](..\uiribbon\ne-uiribbon-ui_fontunderline.md) | Specifies values that identify the underline state of a FontControl. |
| [UI_FONTVERTICALPOSITION enumeration](..\uiribbon\ne-uiribbon-ui_fontverticalposition.md) | Specifies values that identify the vertical-alignment state of a FontControl. |
| [UI_INVALIDATIONS enumeration](..\uiribbon\ne-uiribbon-ui_invalidations.md) | Specifies values that identify the aspect of a Command to invalidate. |
| [UI_OWNERSHIP enumeration](..\uiribbon\ne-uiribbon-ui_ownership.md) | Specifies values that identify the ownership conditions under which an image is created by the Windows Ribbon framework. |
| [UI_SWATCHCOLORMODE enumeration](..\uiribbon\ne-uiribbon-ui_swatchcolormode.md) | Specifies whether a swatch has normal or monochrome mode. |
| [UI_SWATCHCOLORTYPE enumeration](..\uiribbon\ne-uiribbon-ui_swatchcolortype.md) | Specifies the values that identify how a color swatch in a DropDownColorPicker or a FontControl color picker (Text color or Text highlight) is filled.Note  These are recommendations only. |
| [UI_VIEWTYPE enumeration](..\uiribbon\ne-uiribbon-ui_viewtype.md) | Specifies values that identify the Ribbon framework View. |
| [UI_VIEWVERB enumeration](..\uiribbon\ne-uiribbon-ui_viewverb.md) | Specifies values that identify the type of action to complete on a Ribbon framework View. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IUIApplication interface](..\uiribbon\nn-uiribbon-iuiapplication.md) | The IUIApplication interface is implemented by the application and defines the callback entry-point methods for the Windows Ribbon framework. |
| [IUICollection interface](..\uiribbon\nn-uiribbon-iuicollection.md) | The IUICollection interface is implemented by the Ribbon framework. |
| [IUICollectionChangedEvent interface](..\uiribbon\nn-uiribbon-iuicollectionchangedevent.md) | The IUICollectionChangedEvent interface is implemented by the application and defines the method required to handle changes to a collection at run time. |
| [IUICommandHandler interface](..\uiribbon\nn-uiribbon-iuicommandhandler.md) | The IUICommandHandler interface is implemented by the application and defines the methods for gathering Command information and handling Command events from the Windows Ribbon framework. |
| [IUIContextualUI interface](..\uiribbon\nn-uiribbon-iuicontextualui.md) | The IUIContextualUI interface is implemented by the Ribbon framework and provides the core functionality for the Context Popup View. |
| [IUIEventLogger interface](..\uiribbon\nn-uiribbon-iuieventlogger.md) | The IUIEventLogger interface is implemented by the application and defines the ribbon events callback method. |
| [IUIEventingManager interface](..\uiribbon\nn-uiribbon-iuieventingmanager.md) | The IUIEventingManager interface is implemented by the Ribbon framework and provides the notification functionality for applications that register for ribbon events. |
| [IUIFramework interface](..\uiribbon\nn-uiribbon-iuiframework.md) | The IUIFramework interface is implemented by the Windows Ribbon framework and defines the methods that provide the core functionality for the framework. |
| [IUIImage interface](..\uiribbon\nn-uiribbon-iuiimage.md) | The IUIImage interface is implemented by the application and defines the method for retrieving an image to display in the ribbon and context popup UI of the Windows Ribbon framework . |
| [IUIImageFromBitmap interface](..\uiribbon\nn-uiribbon-iuiimagefrombitmap.md) | IUIImageFromBitmap is a factory interface implemented by the Windows Ribbon framework that defines the method for creating an IUIImage object. |
| [IUIRibbon interface](..\uiribbon\nn-uiribbon-iuiribbon.md) | The IUIRibbon interface is implemented by the Windows Ribbon framework and provides the ability to specify settings and properties for a ribbon. |
| [IUISimplePropertySet interface](..\uiribbon\nn-uiribbon-iuisimplepropertyset.md) | IUISimplePropertySet is a read-only interface that defines a method for retrieving the value identified by a property key. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IUIApplication::OnCreateUICommand](..\uiribbon\nf-uiribbon-iuiapplication-oncreateuicommand.md) | Called for each Command specified in the Windows Ribbon framework markup to bind the Command to an IUICommandHandler. |
| [IUIApplication::OnDestroyUICommand](..\uiribbon\nf-uiribbon-iuiapplication-ondestroyuicommand.md) | Called for each Command specified in the Windows Ribbon framework markup when the application window is destroyed. |
| [IUIApplication::OnViewChanged](..\uiribbon\nf-uiribbon-iuiapplication-onviewchanged.md) | Called when the state of a View changes. |
| [IUICollection::Add](..\uiribbon\nf-uiribbon-iuicollection-add.md) | Adds an item to the end of the IUICollection. |
| [IUICollection::Clear](..\uiribbon\nf-uiribbon-iuicollection-clear.md) | Deletes all items from the IUICollection. |
| [IUICollection::GetCount](..\uiribbon\nf-uiribbon-iuicollection-getcount.md) | Retrieves the number of items contained in the IUICollection. |
| [IUICollection::GetItem](..\uiribbon\nf-uiribbon-iuicollection-getitem.md) | Retrieves an item from the IUICollection at the specified index. |
| [IUICollection::Insert](..\uiribbon\nf-uiribbon-iuicollection-insert.md) | Inserts an item into the IUICollection at the specified index. |
| [IUICollection::RemoveAt](..\uiribbon\nf-uiribbon-iuicollection-removeat.md) | Removes an item from the IUICollection at the specified index. |
| [IUICollection::Replace](..\uiribbon\nf-uiribbon-iuicollection-replace.md) | Replaces an item at the specified index of the IUICollection with another item. |
| [IUICollectionChangedEvent::OnChanged](..\uiribbon\nf-uiribbon-iuicollectionchangedevent-onchanged.md) | Called when an IUICollection changes. |
| [IUICommandHandler::Execute](..\uiribbon\nf-uiribbon-iuicommandhandler-execute.md) | Responds to execute events on Commands bound to the Command handler. |
| [IUICommandHandler::UpdateProperty](..\uiribbon\nf-uiribbon-iuicommandhandler-updateproperty.md) | Responds to property update requests from the Windows Ribbon framework. |
| [IUIContextualUI::ShowAtLocation](..\uiribbon\nf-uiribbon-iuicontextualui-showatlocation.md) | Displays a ContextPopup. |
| [IUIEventingManager::SetEventLogger](..\uiribbon\nf-uiribbon-iuieventingmanager-seteventlogger.md) | Sets the event logger for ribbon events. |
| [IUIFramework::Destroy](..\uiribbon\nf-uiribbon-iuiframework-destroy.md) | Terminates and releases all objects, hooks, and references for an instance of the Windows Ribbon framework. |
| [IUIFramework::FlushPendingInvalidations](..\uiribbon\nf-uiribbon-iuiframework-flushpendinginvalidations.md) | Processes all pending Command updates. |
| [IUIFramework::GetUICommandProperty](..\uiribbon\nf-uiribbon-iuiframework-getuicommandproperty.md) | Retrieves a command property, value, or state. |
| [IUIFramework::GetView](..\uiribbon\nf-uiribbon-iuiframework-getview.md) | Retrieves the address of a pointer to an interface that represents a Windows Ribbon framework View, such as IUIRibbon or IUIContextualUI. |
| [IUIFramework::Initialize](..\uiribbon\nf-uiribbon-iuiframework-initialize.md) | Connects the host application to the Windows Ribbon framework. |
| [IUIFramework::InvalidateUICommand](..\uiribbon\nf-uiribbon-iuiframework-invalidateuicommand.md) | Invalidates a Windows Ribbon framework Command property, value, or state. |
| [IUIFramework::LoadUI](..\uiribbon\nf-uiribbon-iuiframework-loadui.md) | Loads the Windows Ribbon framework UI resource, or compiled markup, file. |
| [IUIFramework::SetModes](..\uiribbon\nf-uiribbon-iuiframework-setmodes.md) | Specifies the application modes to enable. |
| [IUIFramework::SetUICommandProperty](..\uiribbon\nf-uiribbon-iuiframework-setuicommandproperty.md) | Sets a command property, value, or state. |
| [IUIImage::GetBitmap](..\uiribbon\nf-uiribbon-iuiimage-getbitmap.md) | Retrieves a bitmap to display as an icon in the ribbon and context popup UI of the Windows Ribbon framework. |
| [IUIImageFromBitmap::CreateImage](..\uiribbon\nf-uiribbon-iuiimagefrombitmap-createimage.md) | Creates an IUIImage object from a bitmap image. |
| [IUIRibbon::GetHeight](..\uiribbon\nf-uiribbon-iuiribbon-getheight.md) | Retrieves the height of the ribbon. |
| [IUIRibbon::LoadSettingsFromStream](..\uiribbon\nf-uiribbon-iuiribbon-loadsettingsfromstream.md) | Reads ribbon settings from a binary stream. |
| [IUIRibbon::SaveSettingsToStream](..\uiribbon\nf-uiribbon-iuiribbon-savesettingstostream.md) | Writes ribbon settings to a binary stream. |
| [IUISimplePropertySet::GetValue](..\uiribbon\nf-uiribbon-iuisimplepropertyset-getvalue.md) | Retrieves the value identified by a property key. |
