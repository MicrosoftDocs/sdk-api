---
UID: TP:wintouch
ms.assetid: 7340eb41-5269-3872-ab0e-7e5a90776681
ms.author: windowssdkdev
ms.date: 06/07/2018
ms.keywords: 
ms.prod: windows
ms.technology: windows-sdk
ms.topic: portal
---

# Touch Input



Overview of the Touch Input technology.

To develop Touch Input, you need these headers:

 * [manipulations.h](..\manipulations\index.md)

For the programming guide, see [Touch Input](/windows/desktop/wintouch).

## Enumerations

| Title   | Description   |
| ---- |:---- |
| [MANIPULATION_PROCESSOR_MANIPULATIONS enumeration](..\manipulations\ne-manipulations-manipulation_processor_manipulations.md) | The MANIPULATION_PROCESSOR_MANIPULATIONS enumeration different kinds of manipulation which can be applied on a target object. |

## Interfaces

| Title   | Description   |
| ---- |:---- |
| [IInertiaProcessor interface](..\manipulations\nn-manipulations-iinertiaprocessor.md) | The IInertiaProcessor interface handles calculations regarding object motion for Windows Touch. |
| [IManipulationProcessor interface](..\manipulations\nn-manipulations-imanipulationprocessor.md) | The IManipulationProcessor provides functionality for monitoring and responding to multitouch input. |
| [_IManipulationEvents interface](..\manipulations\nn-manipulations-_imanipulationevents.md) | Handles manipulation and inertia events. |

## Methods

| Title   | Description   |
| ---- |:---- |
| [IInertiaProcessor::CompleteTime](..\manipulations\nf-manipulations-iinertiaprocessor-completetime.md) | Finishes the current manipulation at the given tick, stops inertia on the inertia processor, and raises the ManipulationCompleted event. |
| [IInertiaProcessor::Complete](..\manipulations\nf-manipulations-iinertiaprocessor-complete.md) | The Complete method finishes the current manipulation and stops inertia on the inertia processor. |
| [IInertiaProcessor::ProcessTime](..\manipulations\nf-manipulations-iinertiaprocessor-processtime.md) | The ProcessTime method performs calculations for the given tick and can raise the Started, Delta, or Completed event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op. |
| [IInertiaProcessor::Process](..\manipulations\nf-manipulations-iinertiaprocessor-process.md) | The Process method performs calculations and can raise the Started, Delta, or Completed event depending on whether extrapolation is completed or not. If extrapolation finished at the previous tick, the method is no-op. |
| [IInertiaProcessor::Reset](..\manipulations\nf-manipulations-iinertiaprocessor-reset.md) | The Reset method initializes the processor with initial timestamp and restarts inertia. |
| [IInertiaProcessor::get_BoundaryBottom](..\manipulations\nf-manipulations-iinertiaprocessor-get_boundarybottom.md) | The BoundaryBottom property limits how far towards the bottom of the screen the target object can move. |
| [IInertiaProcessor::get_BoundaryLeft](..\manipulations\nf-manipulations-iinertiaprocessor-get_boundaryleft.md) | The BoundaryLeft property limits how far towards the left of the screen the target object can move. |
| [IInertiaProcessor::get_BoundaryRight](..\manipulations\nf-manipulations-iinertiaprocessor-get_boundaryright.md) | The BoundaryRight property limits how far towards the right of the screen the target object can move. |
| [IInertiaProcessor::get_BoundaryTop](..\manipulations\nf-manipulations-iinertiaprocessor-get_boundarytop.md) | The BoundaryTop property limits how far towards the top of the screen the target object can move. |
| [IInertiaProcessor::get_DesiredAngularDeceleration](..\manipulations\nf-manipulations-iinertiaprocessor-get_desiredangulardeceleration.md) | The DesiredAngularDeceleration property specifies the desired rate that the target object will stop spinning in radians per msec squared. |
| [IInertiaProcessor::get_DesiredDeceleration](..\manipulations\nf-manipulations-iinertiaprocessor-get_desireddeceleration.md) | The DesiredDeceleration property specifies the desired rate at which translation operations will decelerate. |
| [IInertiaProcessor::get_DesiredDisplacement](..\manipulations\nf-manipulations-iinertiaprocessor-get_desireddisplacement.md) | The DesiredDisplacement property specifies the desired distance that the object will travel. |
| [IInertiaProcessor::get_DesiredExpansionDeceleration](..\manipulations\nf-manipulations-iinertiaprocessor-get_desiredexpansiondeceleration.md) | The DesiredExpansionDeceleration property specifies the rate at which the object will stop expanding. |
| [IInertiaProcessor::get_DesiredExpansion](..\manipulations\nf-manipulations-iinertiaprocessor-get_desiredexpansion.md) | The DesiredExpansion property specifies the desired change in the object's average radius. |
| [IInertiaProcessor::get_DesiredRotation](..\manipulations\nf-manipulations-iinertiaprocessor-get_desiredrotation.md) | The DesiredRotation property specifies how far the current inertia processor object should manipulate the target object in radians. |
| [IInertiaProcessor::get_ElasticMarginBottom](..\manipulations\nf-manipulations-iinertiaprocessor-get_elasticmarginbottom.md) | The ElasticMarginBottom property specifies the bottom region for bouncing the target object. |
| [IInertiaProcessor::get_ElasticMarginLeft](..\manipulations\nf-manipulations-iinertiaprocessor-get_elasticmarginleft.md) | The ElasticMarginLeft property specifies the leftmost region for bouncing the target object. |
| [IInertiaProcessor::get_ElasticMarginRight](..\manipulations\nf-manipulations-iinertiaprocessor-get_elasticmarginright.md) | The ElasticMarginRight property specifies the rightmost region for bouncing the target object. |
| [IInertiaProcessor::get_ElasticMarginTop](..\manipulations\nf-manipulations-iinertiaprocessor-get_elasticmargintop.md) | The ElasticMarginTop property specifies the topmost region for bouncing the target object. |
| [IInertiaProcessor::get_InitialAngularVelocity](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialangularvelocity.md) | The InitialAngularVelocity property specifies the rotational (angular) velocity of the target when movement begins. |
| [IInertiaProcessor::get_InitialExpansionVelocity](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialexpansionvelocity.md) | The InitialExpansionVelocity property specifies the rate of radius expansion for a target when the target was affected by inertia. |
| [IInertiaProcessor::get_InitialOriginX](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialoriginx.md) | The InitialOriginX property specifies the starting horizontal location for a target with inertia. |
| [IInertiaProcessor::get_InitialOriginY](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialoriginy.md) | The InitialOriginY property specifies the starting vertical location for a target with inertia. |
| [IInertiaProcessor::get_InitialRadius](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialradius.md) | The InitialRadius property specifies the distance from the edge of the target to its center before the object was changed. |
| [IInertiaProcessor::get_InitialTimestamp](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialtimestamp.md) | The InitialTimestamp property specifies the starting time stamp for a target object with inertia. |
| [IInertiaProcessor::get_InitialVelocityX](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialvelocityx.md) | The InitialVelocityX property specifies the initial movement of the target object on the horizontal axis. |
| [IInertiaProcessor::get_InitialVelocityY](..\manipulations\nf-manipulations-iinertiaprocessor-get_initialvelocityy.md) | The InitialVelocityY property specifies the initial movement of the target object on the vertical axis. |
| [IInertiaProcessor::put_BoundaryBottom](..\manipulations\nf-manipulations-iinertiaprocessor-put_boundarybottom.md) | The BoundaryBottom property limits how far towards the bottom of the screen the target object can move. |
| [IInertiaProcessor::put_BoundaryLeft](..\manipulations\nf-manipulations-iinertiaprocessor-put_boundaryleft.md) | The BoundaryLeft property limits how far towards the left of the screen the target object can move. |
| [IInertiaProcessor::put_BoundaryRight](..\manipulations\nf-manipulations-iinertiaprocessor-put_boundaryright.md) | The BoundaryRight property limits how far towards the right of the screen the target object can move. |
| [IInertiaProcessor::put_BoundaryTop](..\manipulations\nf-manipulations-iinertiaprocessor-put_boundarytop.md) | The BoundaryTop property limits how far towards the top of the screen the target object can move. |
| [IInertiaProcessor::put_DesiredAngularDeceleration](..\manipulations\nf-manipulations-iinertiaprocessor-put_desiredangulardeceleration.md) | The DesiredAngularDeceleration property specifies the desired rate that the target object will stop spinning in radians per msec squared. |
| [IInertiaProcessor::put_DesiredDeceleration](..\manipulations\nf-manipulations-iinertiaprocessor-put_desireddeceleration.md) | The DesiredDeceleration property specifies the desired rate at which translation operations will decelerate. |
| [IInertiaProcessor::put_DesiredDisplacement](..\manipulations\nf-manipulations-iinertiaprocessor-put_desireddisplacement.md) | The DesiredDisplacement property specifies the desired distance that the object will travel. |
| [IInertiaProcessor::put_DesiredExpansionDeceleration](..\manipulations\nf-manipulations-iinertiaprocessor-put_desiredexpansiondeceleration.md) | The DesiredExpansionDeceleration property specifies the rate at which the object will stop expanding. |
| [IInertiaProcessor::put_DesiredExpansion](..\manipulations\nf-manipulations-iinertiaprocessor-put_desiredexpansion.md) | The DesiredExpansion property specifies the desired change in the object's average radius. |
| [IInertiaProcessor::put_DesiredRotation](..\manipulations\nf-manipulations-iinertiaprocessor-put_desiredrotation.md) | The DesiredRotation property specifies how far the current inertia processor object should manipulate the target object in radians. |
| [IInertiaProcessor::put_ElasticMarginBottom](..\manipulations\nf-manipulations-iinertiaprocessor-put_elasticmarginbottom.md) | The ElasticMarginBottom property specifies the bottom region for bouncing the target object. |
| [IInertiaProcessor::put_ElasticMarginLeft](..\manipulations\nf-manipulations-iinertiaprocessor-put_elasticmarginleft.md) | The ElasticMarginLeft property specifies the leftmost region for bouncing the target object. |
| [IInertiaProcessor::put_ElasticMarginRight](..\manipulations\nf-manipulations-iinertiaprocessor-put_elasticmarginright.md) | The ElasticMarginRight property specifies the rightmost region for bouncing the target object. |
| [IInertiaProcessor::put_ElasticMarginTop](..\manipulations\nf-manipulations-iinertiaprocessor-put_elasticmargintop.md) | The ElasticMarginTop property specifies the topmost region for bouncing the target object. |
| [IInertiaProcessor::put_InitialAngularVelocity](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialangularvelocity.md) | The InitialAngularVelocity property specifies the rotational (angular) velocity of the target when movement begins. |
| [IInertiaProcessor::put_InitialExpansionVelocity](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialexpansionvelocity.md) | The InitialExpansionVelocity property specifies the rate of radius expansion for a target when the target was affected by inertia. |
| [IInertiaProcessor::put_InitialOriginX](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialoriginx.md) | The InitialOriginX property specifies the starting horizontal location for a target with inertia. |
| [IInertiaProcessor::put_InitialOriginY](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialoriginy.md) | The InitialOriginY property specifies the starting vertical location for a target with inertia. |
| [IInertiaProcessor::put_InitialRadius](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialradius.md) | The InitialRadius property specifies the distance from the edge of the target to its center before the object was changed. |
| [IInertiaProcessor::put_InitialTimestamp](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialtimestamp.md) | The InitialTimestamp property specifies the starting time stamp for a target object with inertia. |
| [IInertiaProcessor::put_InitialVelocityX](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialvelocityx.md) | The InitialVelocityX property specifies the initial movement of the target object on the horizontal axis. |
| [IInertiaProcessor::put_InitialVelocityY](..\manipulations\nf-manipulations-iinertiaprocessor-put_initialvelocityy.md) | The InitialVelocityY property specifies the initial movement of the target object on the vertical axis. |
| [IManipulationProcessor::CompleteManipulation](..\manipulations\nf-manipulations-imanipulationprocessor-completemanipulation.md) | The CompleteManipulation method is called when the developer chooses to end the manipulation. |
| [IManipulationProcessor::GetAngularVelocity](..\manipulations\nf-manipulations-imanipulationprocessor-getangularvelocity.md) | The GetAngularVelocity method calculates the rotational velocity that the target object is moving at. |
| [IManipulationProcessor::GetExpansionVelocity](..\manipulations\nf-manipulations-imanipulationprocessor-getexpansionvelocity.md) | The GetExpansionVelocity method calculates the rate that the target object is expanding at. |
| [IManipulationProcessor::GetVelocityX](..\manipulations\nf-manipulations-imanipulationprocessor-getvelocityx.md) | Calculates and returns the horizontal velocity for the target object. |
| [IManipulationProcessor::GetVelocityY](..\manipulations\nf-manipulations-imanipulationprocessor-getvelocityy.md) | Calculates and returns the vertical velocity. |
| [IManipulationProcessor::ProcessDownWithTime](..\manipulations\nf-manipulations-imanipulationprocessor-processdownwithtime.md) | Feeds touch down data, including a timestamp, to the manipulation processor associated with a target. |
| [IManipulationProcessor::ProcessDown](..\manipulations\nf-manipulations-imanipulationprocessor-processdown.md) | The ProcessDown method feeds touch down data to the manipulation processor associated with a target. |
| [IManipulationProcessor::ProcessMoveWithTime](..\manipulations\nf-manipulations-imanipulationprocessor-processmovewithtime.md) | Feeds movement data, including a time stamp, for the target object to its manipulation processor. |
| [IManipulationProcessor::ProcessMove](..\manipulations\nf-manipulations-imanipulationprocessor-processmove.md) | The ProcessMove method feeds movement data for the target object to its manipulation processor. |
| [IManipulationProcessor::ProcessUpWithTime](..\manipulations\nf-manipulations-imanipulationprocessor-processupwithtime.md) | Feeds data, including a timestamp, to a target's manipulation processor for touch-up sequences. |
| [IManipulationProcessor::ProcessUp](..\manipulations\nf-manipulations-imanipulationprocessor-processup.md) | The ProcessUp method feeds data to a target's manipulation processor for touch up sequences. |
| [IManipulationProcessor::get_PivotPointX](..\manipulations\nf-manipulations-imanipulationprocessor-get_pivotpointx.md) | The PivotPointX property is the horizontal center of the object. |
| [IManipulationProcessor::get_PivotPointY](..\manipulations\nf-manipulations-imanipulationprocessor-get_pivotpointy.md) | The PivotPointY property is the vertical center of the object. |
| [IManipulationProcessor::get_PivotRadius](..\manipulations\nf-manipulations-imanipulationprocessor-get_pivotradius.md) | The PivotRadius property is used to determine how much rotation is used in single finger manipulation. |
| [IManipulationProcessor::get_SupportedManipulations](..\manipulations\nf-manipulations-imanipulationprocessor-get_supportedmanipulations.md) | The SupportedManipulations property is used to indicate which manipulations are supported by an object. |
| [IManipulationProcessor::put_PivotPointX](..\manipulations\nf-manipulations-imanipulationprocessor-put_pivotpointx.md) | The PivotPointX property is the horizontal center of the object. |
| [IManipulationProcessor::put_PivotPointY](..\manipulations\nf-manipulations-imanipulationprocessor-put_pivotpointy.md) | The PivotPointY property is the vertical center of the object. |
| [IManipulationProcessor::put_PivotRadius](..\manipulations\nf-manipulations-imanipulationprocessor-put_pivotradius.md) | The PivotRadius property is used to determine how much rotation is used in single finger manipulation. |
| [IManipulationProcessor::put_SupportedManipulations](..\manipulations\nf-manipulations-imanipulationprocessor-put_supportedmanipulations.md) | The SupportedManipulations property is used to indicate which manipulations are supported by an object. |
| [_IManipulationEvents::ManipulationCompleted](..\manipulations\nf-manipulations-_imanipulationevents-manipulationcompleted.md) | Handles the event when manipulation or inertia finishes. |
| [_IManipulationEvents::ManipulationDelta](..\manipulations\nf-manipulations-_imanipulationevents-manipulationdelta.md) | Handles events that happen when a manipulated object changes. |
| [_IManipulationEvents::ManipulationStarted](..\manipulations\nf-manipulations-_imanipulationevents-manipulationstarted.md) | Handles the event for when manipulation or inertia begins. |
