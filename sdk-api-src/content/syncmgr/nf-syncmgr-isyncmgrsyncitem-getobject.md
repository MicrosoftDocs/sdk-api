---
UID: NF:syncmgr.ISyncMgrSyncItem.GetObject
title: ISyncMgrSyncItem::GetObject (syncmgr.h)
description: Creates a specific type of object related to the item.
helpviewer_keywords: ["GetObject","GetObject method [Windows Shell]","GetObject method [Windows Shell]","ISyncMgrSyncItem interface","ISyncMgrSyncItem interface [Windows Shell]","GetObject method","ISyncMgrSyncItem.GetObject","ISyncMgrSyncItem::GetObject","SYNCMGR_OBJECTID_BrowseContent","SYNCMGR_OBJECTID_ConflictStore","SYNCMGR_OBJECTID_EventStore","SYNCMGR_OBJECTID_Icon","SYNCMGR_OBJECTID_QueryBeforeDelete","SYNCMGR_OBJECTID_QueryBeforeDisable","SYNCMGR_OBJECTID_QueryBeforeEnable","_shell_ISyncMgrSyncItem_GetObject","shell.ISyncMgrSyncItem_GetObject","syncmgr/ISyncMgrSyncItem::GetObject"]
old-location: shell\ISyncMgrSyncItem_GetObject.htm
tech.root: shell
ms.assetid: 54336c43-348b-4767-94e4-fe7dc47c0876
ms.date: 12/05/2018
ms.keywords: GetObject, GetObject method [Windows Shell], GetObject method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetObject method, ISyncMgrSyncItem.GetObject, ISyncMgrSyncItem::GetObject, SYNCMGR_OBJECTID_BrowseContent, SYNCMGR_OBJECTID_ConflictStore, SYNCMGR_OBJECTID_EventStore, SYNCMGR_OBJECTID_Icon, SYNCMGR_OBJECTID_QueryBeforeDelete, SYNCMGR_OBJECTID_QueryBeforeDisable, SYNCMGR_OBJECTID_QueryBeforeEnable, _shell_ISyncMgrSyncItem_GetObject, shell.ISyncMgrSyncItem_GetObject, syncmgr/ISyncMgrSyncItem::GetObject
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
 - ISyncMgrSyncItem::GetObject
 - syncmgr/ISyncMgrSyncItem::GetObject
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
 - ISyncMgrSyncItem.GetObject
---

# ISyncMgrSyncItem::GetObject


## -description

Creates a specific type of object related to the item.

## -parameters

### -param rguidObjectID [in]

Type: <b>REFGUID</b>

A GUID identifying the type of object to create. One of the following values as defined in shlguid.h.





#### SYNCMGR_OBJECTID_BrowseContent

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that shows UI that allows the user to browse the contents of the item. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_CAN_BROWSE_CONTENT</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_ConflictStore

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrconflictstore">ISyncMgrConflictStore</a> interface that allows an item to provide conflicts. These conflicts are shown in the Sync Center Conflicts folder. The conflict store should include conflicts only for the item. To include conflicts for all of a handler's items, Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">GetObject</a>. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_CONFLICT_STORE</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_EventStore

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgreventstore">ISyncMgrEventStore</a> interface that allows an item to provide its own source of events. These events are shown in the Sync Results folder. The event store should include only events for the item. To include events for all of a handler's items, Sync Center calls <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandler-getobject">GetObject</a>.

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_EVENT_STORE</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a>.

An item is not required to provide an event store. The default event store provided by Sync Center can be used if it meets the item's requirements.



#### SYNCMGR_OBJECTID_Icon

An icon extraction object that implements the <a href="/windows/desktop/api/shlobj_core/nn-shlobj_core-iextracticona">IExtractIcon</a> interface used to display an icon for the item. This object should only be provided if the item obtains its icon dynamically at run time. The preferred mechanism for providing the icon is to register the icon as the DefaultIcon in the registry.
 
                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_PROVIDES_ICON</a> capability flag is set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_QueryBeforeDelete

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays UI when the user selects the item in the handler's folder then selects the <b>Delete</b> task. Before requesting this object, Sync Center creates both a separate thread for this operation and a new instance of the item.

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_CAN_DELETE</a> and <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_QUERY_BEFORE_DELETE</a> capability flags are set in the mask retrieved by <a href="/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrsyncitem-getcapabilities">GetCapabilities</a>.



#### SYNCMGR_OBJECTID_QueryBeforeEnable

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays UI when the user selects the item in the Sync Center folder then selects the <b>Enable</b> task. Before requesting this object, Sync Center creates both a separate thread for this operation and a new instance of the item.

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_QUERY_BEFORE_ENABLE</a> capability flag is set and the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_policies">SYNCMGR_IPM_PREVENT_ENABLE</a> policy flag is not.



#### SYNCMGR_OBJECTID_QueryBeforeDisable

An object implementing the <a href="/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgruioperation">ISyncMgrUIOperation</a> interface that displays UI when the user selects the item in the handler's folder then selects the <b>Disable</b> task. Before requesting this object, Sync Center creates both a separate thread for this operation and a new instance of the item. 

                        

Sync Center only requests this object if the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_capabilities">SYNCMGR_ICM_QUERY_BEFORE_DELETE</a> capability flag is set and the <a href="/windows/desktop/api/syncmgr/ne-syncmgr-syncmgr_item_policies">SYNCMGR_IPM_PREVENT_DISABLE</a> policy flag is not.

### -param riid [in]

Type: <b>REFIID</b>

The IID of the requested interface. This is dependent on the object type named in <i>rguidObjectID</i>.

### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of a pointer to the requested interface.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. Returns E_INVALIDARG if the item does not support the requested type of object.

## -remarks

The item can implement the requested interface on its handler or it can implement it on a different object.


#### Examples



The following example shows an implementation of this method.


```cpp
STDMETHODIMP CMyDeviceSyncItem::GetObject(__in REFGUID   rguidObjectID,
                                          __in REFIID    riid,
                                          __out void   **ppv)
{
    HRESULT hr = E_INVALIDARG;
    *ppv = NULL;

    if (rguidObjectID == SYNCMGR_OBJECTID_QueryBeforeDelete)
    {
        hr = _CreateQueryBeforeDeleteObject(riid, ppv);
    }
    else if (rguidObjectID == SYNCMGR_OBJECTID_EventStore)
    {
        hr = _CreateEventStore(_pszItemID, riid, ppv);
    }

    return hr;
}

```