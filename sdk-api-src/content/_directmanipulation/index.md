---
UID: TP:directmanipulation
ms.assetid: b4054831-982d-3b85-96f1-a2f6819aac6a
ms.author: windowssdkdev
ms.date: 06/08/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
archived: true
---

# Direct Manipulation

## -description

Overview of the Direct Manipulation technology.

To develop Direct Manipulation, you need these headers:

 * [directmanipulation.h](..\directmanipulation\index.md)

For the programming guide, see [Direct Manipulation](/previous-versions/windows/desktop/directmanipulation).

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [DIRECTMANIPULATION_AUTOSCROLL_CONFIGURATION enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_autoscroll_configuration.md) | Determines the type and direction of automatic scrolling animation to apply. |
| [DIRECTMANIPULATION_CONFIGURATION enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_configuration.md) | Defines the interaction configuration states available in Direct Manipulation. |
| [DIRECTMANIPULATION_DRAG_DROP_CONFIGURATION enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_drag_drop_configuration.md) | Defines behaviors for the drag-drop interaction. |
| [DIRECTMANIPULATION_DRAG_DROP_STATUS enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_drag_drop_status.md) | Defines the drag-and-drop interaction states for the viewport. |
| [DIRECTMANIPULATION_GESTURE_CONFIGURATION enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_gesture_configuration.md) | Defines the gestures that can be passed to SetManualGesture. |
| [DIRECTMANIPULATION_HITTEST_TYPE enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_hittest_type.md) | Defines how hit testing is handled by Direct Manipulation when using a dedicated hit-test thread registered through RegisterHitTestTarget. |
| [DIRECTMANIPULATION_HORIZONTALALIGNMENT enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_horizontalalignment.md) | Defines the horizontal alignment options for content within a viewport. |
| [DIRECTMANIPULATION_INPUT_MODE enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_input_mode.md) | Defines the threading behavior for SetInputMode or SetUpdateMode. The exact meaning of each constant depends on the method called. |
| [DIRECTMANIPULATION_INTERACTION_TYPE enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_interaction_type.md) | Defines gestures recognized by Direct Manipulation. |
| [DIRECTMANIPULATION_MOTION_TYPES enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_motion_types.md) | Defines the Direct Manipulation motion type. |
| [DIRECTMANIPULATION_SNAPPOINT_COORDINATE enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_snappoint_coordinate.md) | Defines the coordinate system for a collection of snap points. |
| [DIRECTMANIPULATION_SNAPPOINT_TYPE enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_snappoint_type.md) | Modifies how the final inertia end position is calculated. |
| [DIRECTMANIPULATION_STATUS enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_status.md) | Defines the possible states of Direct Manipulation. |
| [DIRECTMANIPULATION_VERTICALALIGNMENT enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_verticalalignment.md) | Defines the vertical alignment settings for content within the viewport. |
| [DIRECTMANIPULATION_VIEWPORT_OPTIONS enumeration](..\directmanipulation\ne-directmanipulation-directmanipulation_viewport_options.md) | Defines the input behavior options for the viewport. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IDirectManipulationAutoScrollBehavior interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationautoscrollbehavior.md) | Represents the auto-scroll animation behavior of content as it approaches the boundary of a given axis or axes. |
| [IDirectManipulationCompositor interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationcompositor.md) | Represents a compositor object that associates manipulated content with a drawing surface, such as canvas (Windows app using JavaScript) or Canvas (Windows Store app using C++, C#, or Visual Basic). |
| [IDirectManipulationCompositor2 interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationcompositor2.md) | Represents a compositor object that associates manipulated content with drawing surfaces across multiple processes. |
| [IDirectManipulationContent interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationcontent.md) | Encapsulates content inside a viewport, where content represents a visual surface clipped inside the viewport. |
| [IDirectManipulationDeferContactService interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationdefercontactservice.md) | Represents a service for managing associations between a contact and a viewport. |
| [IDirectManipulationDragDropBehavior interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationdragdropbehavior.md) | Represents behaviors for drag and drop interactions, which are triggered by cross-slide or press-and-hold gestures. |
| [IDirectManipulationDragDropEventHandler interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationdragdropeventhandler.md) | Defines methods to handle drag-drop behavior events. |
| [IDirectManipulationFrameInfoProvider interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationframeinfoprovider.md) | Represents a time-keeping object that measures the latency of the composition infrastructure used by the application and provides this data to Direct Manipulation. |
| [IDirectManipulationInteractionEventHandler interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationinteractioneventhandler.md) | Defines methods to handle interactions when they are detected. |
| [IDirectManipulationManager interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationmanager.md) | Provides access to all the Direct Manipulation features and APIs available to the client application. |
| [IDirectManipulationManager2 interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationmanager2.md) | Extends the IDirectManipulationManager interface that provides access to all the Direct Manipulation features and APIs available to the client application. |
| [IDirectManipulationManager3 interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationmanager3.md) | Extends the IDirectManipulationManager2 interface that provides access to all the Direct Manipulation features and APIs available to the client application. |
| [IDirectManipulationPrimaryContent interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationprimarycontent.md) | Encapsulates the primary content inside a viewport. |
| [IDirectManipulationUpdateHandler interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationupdatehandler.md) | Defines methods for handling manipulation update events. |
| [IDirectManipulationUpdateManager interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationupdatemanager.md) | Manages how compositor updates are sent to Direct Manipulation. |
| [IDirectManipulationViewport interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationviewport.md) | Defines a region within a window (referred to as a viewport) that is able to receive and process input from user interactions. |
| [IDirectManipulationViewport2 interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationviewport2.md) | Provides management of behaviors on a viewport. A behavior affects the functionality of a particular part of the Direct Manipulation workflow. |
| [IDirectManipulationViewportEventHandler interface](..\directmanipulation\nn-directmanipulation-idirectmanipulationviewporteventhandler.md) | Defines methods for handling status and update events for the viewport. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IDirectManipulationAutoScrollBehavior::SetConfiguration](..\directmanipulation\nf-directmanipulation-idirectmanipulationautoscrollbehavior-setconfiguration.md) | Performs the auto-scroll animation for the viewport this behavior is attached to. |
| [IDirectManipulationCompositor2::AddContentWithCrossProcessChaining](..\directmanipulation\nf-directmanipulation-idirectmanipulationcompositor2-addcontentwithcrossprocesschaining.md) | Associates content (owned by the component host) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals. |
| [IDirectManipulationCompositor::AddContent](..\directmanipulation\nf-directmanipulation-idirectmanipulationcompositor-addcontent.md) | Associates content (owned by the caller) with the compositor, assigns a composition device to the content, and specifies the position of the content in the composition tree relative to other composition visuals. |
| [IDirectManipulationCompositor::Flush](..\directmanipulation\nf-directmanipulation-idirectmanipulationcompositor-flush.md) | Commits all pending updates in the compositor to the system for rendering. |
| [IDirectManipulationCompositor::RemoveContent](..\directmanipulation\nf-directmanipulation-idirectmanipulationcompositor-removecontent.md) | Removes content from the compositor. |
| [IDirectManipulationCompositor::SetUpdateManager](..\directmanipulation\nf-directmanipulation-idirectmanipulationcompositor-setupdatemanager.md) | Sets the update manager used to send compositor updates to Direct Manipulation. |
| [IDirectManipulationContent::GetContentRect](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-getcontentrect.md) | Retrieves the bounding rectangle of the content, relative to the bounding rectangle of the viewport (if defined). |
| [IDirectManipulationContent::GetContentTransform](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-getcontenttransform.md) | Retrieves the transform applied to the content. |
| [IDirectManipulationContent::GetOutputTransform](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-getoutputtransform.md) | Gets the final transform applied to the content. |
| [IDirectManipulationContent::GetTag](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-gettag.md) | Retrieves the tag object set on this content. |
| [IDirectManipulationContent::GetViewport](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-getviewport.md) | Retrieves the viewport that contains the content. |
| [IDirectManipulationContent::SetContentRect](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-setcontentrect.md) | Specifies the bounding rectangle of the content, relative to its viewport. |
| [IDirectManipulationContent::SetTag](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-settag.md) | Specifies the tag object for the content. |
| [IDirectManipulationContent::SyncContentTransform](..\directmanipulation\nf-directmanipulation-idirectmanipulationcontent-synccontenttransform.md) | Modifies the content transform while maintaining the output transform. |
| [IDirectManipulationDeferContactService::CancelContact](..\directmanipulation\nf-directmanipulation-idirectmanipulationdefercontactservice-cancelcontact.md) | Cancel all scheduled calls to SetContact for this pointerId. |
| [IDirectManipulationDeferContactService::CancelDeferral](..\directmanipulation\nf-directmanipulation-idirectmanipulationdefercontactservice-canceldeferral.md) | Cancel the deferral set in DeferContact and process the scheduled SetContact call for this pointerId. |
| [IDirectManipulationDeferContactService::DeferContact](..\directmanipulation\nf-directmanipulation-idirectmanipulationdefercontactservice-defercontact.md) | Specifies the amount of time to defer the execution of a call to SetContact for this pointerId. |
| [IDirectManipulationDragDropBehavior::GetStatus](..\directmanipulation\nf-directmanipulation-idirectmanipulationdragdropbehavior-getstatus.md) | Gets the status of the drag-drop interaction for the viewport this behavior is attached to. |
| [IDirectManipulationDragDropBehavior::SetConfiguration](..\directmanipulation\nf-directmanipulation-idirectmanipulationdragdropbehavior-setconfiguration.md) | Sets the configuration of the drag-drop interaction for the viewport this behavior is attached to. |
| [IDirectManipulationDragDropEventHandler::OnDragDropStatusChange](..\directmanipulation\nf-directmanipulation-idirectmanipulationdragdropeventhandler-ondragdropstatuschange.md) | Called when a status change happens in the viewport that the drag-and-drop behavior is attached to. |
| [IDirectManipulationFrameInfoProvider::GetNextFrameInfo](..\directmanipulation\nf-directmanipulation-idirectmanipulationframeinfoprovider-getnextframeinfo.md) | Retrieves the composition timing information from the compositor. |
| [IDirectManipulationInteractionEventHandler::OnInteraction](..\directmanipulation\nf-directmanipulation-idirectmanipulationinteractioneventhandler-oninteraction.md) | Called when an interaction is detected. |
| [IDirectManipulationManager2::CreateBehavior](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager2-createbehavior.md) | Factory method to create a behavior. |
| [IDirectManipulationManager3::GetService](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager3-getservice.md) | Retrieves an IDirectManipulationDeferContactService object. |
| [IDirectManipulationManager::Activate](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager-activate.md) | Activates Direct Manipulation for processing input and handling callbacks on the specified window. |
| [IDirectManipulationManager::CreateContent](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager-createcontent.md) | The factory method that is used to create an instance of secondary content (such as a panning indicator) inside a viewport. |
| [IDirectManipulationManager::CreateViewport](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager-createviewport.md) | The factory method that is used to create a new IDirectManipulationViewport object. |
| [IDirectManipulationManager::Deactivate](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager-deactivate.md) | Deactivates Direct Manipulation for processing input and handling callbacks on the specified window. |
| [IDirectManipulationManager::GetUpdateManager](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager-getupdatemanager.md) | Gets a pointer to an IDirectManipulationUpdateManager object that receives compositor updates. |
| [IDirectManipulationManager::ProcessInput](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager-processinput.md) | Passes keyboard and mouse messages to the manipulation manager on the app's UI thread. |
| [IDirectManipulationManager::RegisterHitTestTarget](..\directmanipulation\nf-directmanipulation-idirectmanipulationmanager-registerhittesttarget.md) | Registers a dedicated thread for hit testing. |
| [IDirectManipulationPrimaryContent::GetCenterPoint](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-getcenterpoint.md) | Retrieves the center point of the manipulation in content coordinates. |
| [IDirectManipulationPrimaryContent::GetInertiaEndTransform](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-getinertiaendtransform.md) | Gets the final transform, including inertia, of the primary content. |
| [IDirectManipulationPrimaryContent::SetHorizontalAlignment](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-sethorizontalalignment.md) | Sets the horizontal alignment of the primary content relative to the viewport. |
| [IDirectManipulationPrimaryContent::SetSnapCoordinate](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-setsnapcoordinate.md) | Specifies the coordinate system for snap points or snap intervals. |
| [IDirectManipulationPrimaryContent::SetSnapInterval](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-setsnapinterval.md) | Specifies snap points for the inertia end position at uniform intervals. |
| [IDirectManipulationPrimaryContent::SetSnapPoints](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-setsnappoints.md) | Specifies the snap points for the inertia rest position. |
| [IDirectManipulationPrimaryContent::SetSnapType](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-setsnaptype.md) | Specifies the type of snap point. |
| [IDirectManipulationPrimaryContent::SetVerticalAlignment](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-setverticalalignment.md) | Specifies the vertical alignment of the primary content in the viewport. |
| [IDirectManipulationPrimaryContent::SetZoomBoundaries](..\directmanipulation\nf-directmanipulation-idirectmanipulationprimarycontent-setzoomboundaries.md) | Specifies the minimum and maximum boundaries for zoom. |
| [IDirectManipulationUpdateHandler::Update](..\directmanipulation\nf-directmanipulation-idirectmanipulationupdatehandler-update.md) | Notifies the compositor when to update inertia animation. |
| [IDirectManipulationUpdateManager::RegisterWaitHandleCallback](..\directmanipulation\nf-directmanipulation-idirectmanipulationupdatemanager-registerwaithandlecallback.md) | Registers a callback that is triggered by a handle. |
| [IDirectManipulationUpdateManager::UnregisterWaitHandleCallback](..\directmanipulation\nf-directmanipulation-idirectmanipulationupdatemanager-unregisterwaithandlecallback.md) | Deregisters a callback. |
| [IDirectManipulationUpdateManager::Update](..\directmanipulation\nf-directmanipulation-idirectmanipulationupdatemanager-update.md) | Updates Direct Manipulation at the current time. |
| [IDirectManipulationViewport2::AddBehavior](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport2-addbehavior.md) | Adds a behavior to the viewport and returns a cookie to the caller. |
| [IDirectManipulationViewport2::RemoveAllBehaviors](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport2-removeallbehaviors.md) | Removes all behaviors added to the viewport. |
| [IDirectManipulationViewport2::RemoveBehavior](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport2-removebehavior.md) | Removes a behavior from the viewport that matches the given cookie. |
| [IDirectManipulationViewport::Abandon](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-abandon.md) | Releases all resources that are used by the viewport and prepares it for destruction from memory. |
| [IDirectManipulationViewport::ActivateConfiguration](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-activateconfiguration.md) | Sets the configuration for input interaction. |
| [IDirectManipulationViewport::AddConfiguration](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-addconfiguration.md) | Adds an interaction configuration for the viewport. |
| [IDirectManipulationViewport::AddContent](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-addcontent.md) | Adds secondary content, such as a panning indicator, to a viewport. |
| [IDirectManipulationViewport::AddEventHandler](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-addeventhandler.md) | Adds a new event handler to listen for viewport events. |
| [IDirectManipulationViewport::Disable](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-disable.md) | Stops input processing by the viewport. |
| [IDirectManipulationViewport::Enable](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-enable.md) | Starts or resumes input processing by the viewport. |
| [IDirectManipulationViewport::GetPrimaryContent](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-getprimarycontent.md) | Gets the primary content of a viewport that implements IDirectManipulationContent and IDirectManipulationPrimaryContent. |
| [IDirectManipulationViewport::GetStatus](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-getstatus.md) | Gets the state of the viewport. |
| [IDirectManipulationViewport::GetTag](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-gettag.md) | Gets the tag value of a viewport. |
| [IDirectManipulationViewport::GetViewportRect](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-getviewportrect.md) | Retrieves the rectangle for the viewport relative to the origin of the viewport coordinate system specified by SetViewportRect. |
| [IDirectManipulationViewport::ReleaseAllContacts](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-releaseallcontacts.md) | Removes all contacts that are associated with the viewport. Inertia is started if the viewport supports inertia. |
| [IDirectManipulationViewport::ReleaseContact](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-releasecontact.md) | Removes a contact that is associated with a viewport. |
| [IDirectManipulationViewport::RemoveConfiguration](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-removeconfiguration.md) | Removes an interaction configuration for the viewport. |
| [IDirectManipulationViewport::RemoveContent](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-removecontent.md) | Removes secondary content from a viewport. |
| [IDirectManipulationViewport::RemoveEventHandler](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-removeeventhandler.md) | Removes an existing event handler from the viewport. |
| [IDirectManipulationViewport::SetChaining](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setchaining.md) | Specifies the motion types supported in a viewport that can be chained to a parent viewport. |
| [IDirectManipulationViewport::SetContact](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setcontact.md) | Specifies an association between a contact and the viewport. |
| [IDirectManipulationViewport::SetInputMode](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setinputmode.md) | Specifies if input is visible to the UI thread. |
| [IDirectManipulationViewport::SetManualGesture](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setmanualgesture.md) | Sets which gestures are ignored by Direct Manipulation. |
| [IDirectManipulationViewport::SetTag](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-settag.md) | Sets a viewport tag. |
| [IDirectManipulationViewport::SetUpdateMode](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setupdatemode.md) | Specifies whether a viewport updates content manually instead of during an input event. |
| [IDirectManipulationViewport::SetViewportOptions](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setviewportoptions.md) | Sets how the viewport handles input and output. |
| [IDirectManipulationViewport::SetViewportRect](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setviewportrect.md) | Sets the bounding rectangle for the viewport, relative to the origin of the viewport coordinate system. |
| [IDirectManipulationViewport::SetViewportTransform](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-setviewporttransform.md) | Specifies the transform from the viewport coordinate system to the window client coordinate system. |
| [IDirectManipulationViewport::Stop](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-stop.md) | Stops the manipulation and returns the viewport to a ready state. |
| [IDirectManipulationViewport::SyncDisplayTransform](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-syncdisplaytransform.md) | Specifies a display transform for the viewport, and synchronizes the output transform with the new value of the display transform. |
| [IDirectManipulationViewport::ZoomToRect](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewport-zoomtorect.md) | Moves the viewport to a specific area of the primary content and specifies whether to animate the transition. |
| [IDirectManipulationViewportEventHandler::OnContentUpdated](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewporteventhandler-oncontentupdated.md) | Called when content inside a viewport is updated. |
| [IDirectManipulationViewportEventHandler::OnViewportStatusChanged](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewporteventhandler-onviewportstatuschanged.md) | Called when the status of a viewport changes. |
| [IDirectManipulationViewportEventHandler::OnViewportUpdated](..\directmanipulation\nf-directmanipulation-idirectmanipulationviewporteventhandler-onviewportupdated.md) | Called after all content in the viewport has been updated. |
