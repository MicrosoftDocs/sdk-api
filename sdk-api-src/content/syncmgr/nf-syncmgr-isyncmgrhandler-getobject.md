---
UID: NF:syncmgr.ISyncMgrHandler.GetObject
title: ISyncMgrHandler::GetObject (syncmgr.h)
description: Creates a specific type of object related to the handler.
helpviewer_keywords: ["GetObject","GetObject method [Windows Shell]","GetObject method [Windows Shell]","ISyncMgrHandler interface","ISyncMgrHandler interface [Windows Shell]","GetObject method","ISyncMgrHandler.GetObject","ISyncMgrHandler::GetObject","SYNCMGR_OBJECTID_BrowseContent","SYNCMGR_OBJECTID_ConflictStore","SYNCMGR_OBJECTID_EventLinkClick","SYNCMGR_OBJECTID_EventStore","SYNCMGR_OBJECTID_Icon","SYNCMGR_OBJECTID_QueryBeforeActivate","SYNCMGR_OBJECTID_QueryBeforeDeactivate","SYNCMGR_OBJECTID_QueryBeforeDisable","SYNCMGR_OBJECTID_QueryBeforeEnable","SYNCMGR_OBJECTID_ShowSchedule","_shell_ISyncMgrHandler_GetObject","shell.ISyncMgrHandler_GetObject","syncmgr/ISyncMgrHandler::GetObject"]
old-location: shell\ISyncMgrHandler_GetObject.htm
tech.root: shell
ms.assetid: 91441b28-a2d8-4114-86dd-9a3e826deef4
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Windows Shell], GetObject method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetObject method, ISyncMgrHandler.GetObject, ISyncMgrHandler::GetObject, SYNCMGR_OBJECTID_BrowseContent, SYNCMGR_OBJECTID_ConflictStore, SYNCMGR_OBJECTID_EventLinkClick, SYNCMGR_OBJECTID_EventStore, SYNCMGR_OBJECTID_Icon, SYNCMGR_OBJECTID_QueryBeforeActivate, SYNCMGR_OBJECTID_QueryBeforeDeactivate, SYNCMGR_OBJECTID_QueryBeforeDisable, SYNCMGR_OBJECTID_QueryBeforeEnable, SYNCMGR_OBJECTID_ShowSchedule, _shell_ISyncMgrHandler_GetObject, shell.ISyncMgrHandler_GetObject, syncmgr/ISyncMgrHandler::GetObject
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrHandler::GetObject
 - syncmgr/ISyncMgrHandler::GetObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrHandler.GetObject
---

# ISyncMgrHandler::GetObject


## -description

Creates a specific type of object related to the handler.

## -parameters

### -param rguidObjectID [in]

Type: <b>REFGUID</b>

A GUID identifying the type of object to create. One of the following values as defined in shlguid.h.





#### SYNCMGR_OBJECTID_BrowseContent

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that shows the UI that enables the user to browse the contents of the item managed by the handler, such as a folder, device, computer on a network, or an application.

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_CAN_BROWSE_CONTENT</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_ConflictStore

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictstore">ISyncMgrConflictStore</a> interface that enables a handler to provide conflicts. These conflicts are shown in the Sync Center Conflicts folder. The conflict store should include conflicts for the handler as well as conflicts for all of its items. To include conflicts for only a specific item, Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">GetObject</a>. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_CONFLICT_STORE</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_EventLinkClick

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgreventlinkuioperation">ISyncMgrEventLinkUIOperation</a> interface that implements the click action for a link provided on an event displayed in the Sync Results folder.



#### SYNCMGR_OBJECTID_EventStore

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgreventstore">ISyncMgrEventStore</a> interface that allows a handler to provide its own source of events. These events are shown in the Sync Results folder. The event store should include events for the handler as well as for all of its items. To include only events for a specific item, Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getobject">GetObject</a>. The event store is asked to delete the handler's events the next time the handler is synchronized. The default event store purges its events when the user logs off.

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_EVENT_STORE</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>.

A handler is not required to provide an event store. The default event store provided by Sync Center can be used if it meets the handler's requirements.



#### SYNCMGR_OBJECTID_Icon

An icon extraction object that implements the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a> interface used to display an icon for the handler. This object should only be provided if the handler obtains its icon dynamically at run time. The preferred mechanism for providing the icon is to register the icon as the DefaultIcon in the registry.
 
                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_PROVIDES_ICON</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_QueryBeforeActivate

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays the UI that enables the user to configure a handler. This UI is shown when the user selects the handler in the Sync Setup folder, then selects the <b>Setup</b> task. Before requesting this object, Sync Center creates a separate thread for this operation and a new instance of the handler. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a> and the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HPM_PREVENT_ACTIVATE</a> policy flag is not set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getpolicies">GetPolicies</a>.



#### SYNCMGR_OBJECTID_QueryBeforeDeactivate

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays the UI when the user selects the handler in the Sync Center folder, then selects the <b>Delete</b> task. Before requesting this object, Sync Center creates a separate thread for this operation and a new instance of the handler. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_DEACTIVATE</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a> and the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_policies">SYNCMGR_HPM_PREVENT_DEACTIVATE</a> policy flag is not set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getpolicies">GetPolicies</a>.



#### SYNCMGR_OBJECTID_QueryBeforeEnable

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays the UI when the user selects the handler in the Sync Center folder and then selects the <b>Enable</b> task. Before requesting this object, Sync Center creates a separate thread for this operation and a new instance of the handler.

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_CAN_ENABLE</a> and <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_ENABLE</a> capability flags are set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_QueryBeforeDisable

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays the UI when the user selects the handler in the Sync Center folder and then selects the <b>Disable</b> task. Before requesting this object, Sync Center creates both a separate thread for this operation and a new instance of the handler. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_CAN_DISABLE</a> and <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_QUERY_BEFORE_DISABLE</a> capability flags are set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_ShowSchedule

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays the UI that enables the user to configure the schedule for the handler. Before requesting this object, Sync Center creates a separate thread for this operation and a new instance of the handler. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_handler_capabilities">SYNCMGR_HCM_CAN_SHOW_SCHEDULE</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getcapabilities">GetCapabilities</a>.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the requested interface. This depends on the object type named in <i>rguidObjectID</i>.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the requested interface.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns E_NOTIMPL if the handler does not support the requested type of object.

## -remarks

The handler can implement the requested interface on itself or it can implement it on a different object.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceHandler::GetObject( __in REFGUID   rguidObjectID, 
                                          __in REFIID    riid,
                                          __out void   **ppv)
{
    HRESULT hr = E_NOTIMPL;
    *ppv = NULL;

    if (rguidObjectID == SYNCMGR_OBJECTID_QueryBeforeActivate)
    {
        hr = _CreateSetupObject(riid, ppv);
    }
    else if (rguidObjectID == SYNCMGR_OBJECTID_EventStore)
    {
        hr = _CreateEventStore(NULL, riid, ppv);
    }

    return hr;
}

```