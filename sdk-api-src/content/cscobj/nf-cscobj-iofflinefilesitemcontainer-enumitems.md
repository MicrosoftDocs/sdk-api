---
UID: NF:cscobj.IOfflineFilesItemContainer.EnumItems
title: IOfflineFilesItemContainer::EnumItems (cscobj.h)
description: Returns an enumerator of child items for the cache item implementing this method. (IOfflineFilesItemContainer.EnumItems)
helpviewer_keywords: ["EnumItems","EnumItems method [Offline Files]","EnumItems method [Offline Files]","IOfflineFilesItemContainer interface","IOfflineFilesItemContainer interface [Offline Files]","EnumItems method","IOfflineFilesItemContainer.EnumItems","IOfflineFilesItemContainer::EnumItems","OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE","OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE","OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT","OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT","OFFLINEFILES_ITEM_QUERY_REMOTEINFO","cscobj/IOfflineFilesItemContainer::EnumItems","of.iofflinefilesitemcontainer_enumitems"]
old-location: of\iofflinefilesitemcontainer_enumitems.htm
tech.root: of
ms.assetid: 9960e8f8-4d15-4a53-aa77-d0105b6a59d1
ms.date: 12/05/2018
ms.keywords: EnumItems, EnumItems method [Offline Files], EnumItems method [Offline Files],IOfflineFilesItemContainer interface, IOfflineFilesItemContainer interface [Offline Files],EnumItems method, IOfflineFilesItemContainer.EnumItems, IOfflineFilesItemContainer::EnumItems, OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE, OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE, OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEINFO, cscobj/IOfflineFilesItemContainer::EnumItems, of.iofflinefilesitemcontainer_enumitems
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IOfflineFilesItemContainer::EnumItems
 - cscobj/IOfflineFilesItemContainer::EnumItems
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesItemContainer.EnumItems
---

# IOfflineFilesItemContainer::EnumItems


## -description

Returns an enumerator of child items for the cache item implementing this method. Server, share, and directory entries in the Offline Files cache implement this method to expose the enumeration of their immediate children.
<div class="alert"><b>Note</b>  A call to <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> to query a file item for <b>IID_IOfflineFilesItemContainer</b> fails with <b>E_NOINTERFACE</b>, because file items have no children.</div><div> </div>

## -parameters

### -param dwQueryFlags [in]

Flags affecting the amount of query activity at the time of enumeration.  The parameter may contain one or more of the following bit flags.



#### OFFLINEFILES_ITEM_QUERY_REMOTEINFO (0x00000001)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE (0x00000002)

If this flag is set, the enumeration operation includes an extra call to the Offline Files store to obtain information about the connection state (online or offline) of the item.  If this flag is not set, enumeration does not include this extra operation, and connection information will be automatically queried on demand when it is needed.



#### OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT (0x00000004)

If this flag is set, the find operation includes an extra call to the Offline Files store to obtain information about the amount, in bytes, of unsynchronized ("dirty") data for the associated file in the local Offline Files cache.



#### OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT (0x00000008)

This flag is reserved for future use.



#### OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE (0x00000010)

Allows administrators to find items cached by any user. If this flag is set and the caller is not an administrator, the method call fails.

### -param ppenum [out]

Enumerator of <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a> interface pointers.

## -returns

Returns <b>S_OK</b> if successful, or an error value otherwise.

## -remarks

To begin a top-down enumeration of the entire cache, perform the following steps:

<ol>
<li>Create an instance of <b>CLSID_OfflineFilesCache</b> and obtain its <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a> interface.</li>
<li>Call the <b>EnumItems</b> method to obtain an enumerator for the server entries.</li>
<li>For each entry returned, call <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> for  <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a>.</li>
<li>If <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> succeeds, the item supports children.  If so, enumerate each child, calling <b>QueryInterface</b> for <a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a> on each.  This pattern may be recursively applied to enumerate the entire cache.</li>
</ol>

#### Examples

This example illustrates how to perform a top-down traversal of the Offline Files cache using a simple recursive implementation.


```cpp
HRESULT EnumItems(IOfflineFilesItemContainer *pContainer);

//
// Emits the item's path string to the console.
//
HRESULT ReportItem(
    IOfflineFilesItem *pItem
    )
{
    LPWSTR pszPath;
    HRESULT hr = pItem->GetPath(&pszPath);
    if (SUCCEEDED(hr))
    {
        LPCWSTR pszType = L"";
        OFFLINEFILES_ITEM_TYPE ItemType;
        hr = pItem->GetItemType(&ItemType);
        if (SUCCEEDED(hr))
        {
            switch(ItemType)
            {
                case OFFLINEFILES_ITEM_TYPE_SERVER:
                    pszType = L" [SERVER]";
                    break;

                case OFFLINEFILES_ITEM_TYPE_SHARE:
                    pszType = L" [SHARE]";
                    break;

                case OFFLINEFILES_ITEM_TYPE_DIRECTORY:
                    pszType = L" [DIR]";
                    break;

                default:
                    break;
            }
            wprintf(L"%s%s", pszPath, pszType);
        }
        CoTaskMemFree(pszPath);
    }
    return hr;
}

//
// Processes the "current" item then recursively enumerate children
// if the item is a container (server, share, directory).
//
HRESULT ProcessItem(
    IOfflineFilesItem *pItem
    )
{
    HRESULT hr = ReportItem(pItem);
    if (SUCCEEDED(hr))
    {
        IOfflineFilesItemContainer *pContainer;
        hr = pItem->QueryInterface(IID_IOfflineFilesItemContainer,
                                   (void **)&pContainer);
        if (SUCCEEDED(hr))
        {
            EnumItems(pContainer);
            pContainer->Release();
        }
    }
    return hr;
}

//
// Enumerate the items in a container.
//
HRESULT EnumItems(
    IOfflineFilesItemContainer *pContainer
    )
{
    IEnumOfflineFilesItems *pEnum;
    HRESULT hr = pContainer->EnumItems(0, &pEnum);
    if (SUCCEEDED(hr))
    {
        IOfflineFilesItem *pItem;
        ULONG celt;
        while(S_OK == (hr = pEnum->Next(1, &pItem, &celt)))
        {
            ProcessItem(pItem);
            pItem->Release();
        }
        pEnum->Release();
    }
    return hr;
}

HRESULT EnumItemsInCache(
    IOfflineFilesCache *pCache
    )
{
    //
    // The "cache" object is a container of "server" items.
    //
    IOfflineFilesItemContainer *pContainer;
    HRESULT hr = pCache->QueryInterface(IID_IOfflineFilesItemContainer,
                                        (void **)&pContainer);
    if (SUCCEEDED(hr))
    {
        hr = EnumItems(pContainer);
    }
    return hr;
}

int wmain(int argc, __in_ecount(argc) WCHAR* argv[])
{
    HRESULT hr = CoInitialize(NULL);
    if (SUCCEEDED(hr))
    {
        //
        // The "cache" object is the entry point into the
        // Offline Files COM API.
        //
        IOfflineFilesCache *pCache;
        hr = CoCreateInstance(CLSID_OfflineFilesCache,
                              NULL,
                              CLSCTX_INPROC_SERVER,
                              IID_IOfflineFilesCache,
                              (void **)&pCache);
        if (SUCCEEDED(hr))
        {
            hr = EnumItemsInCache(pCache);
            pCache->Release();
        }
        CoUninitialize();
    }
    return 0;
}

```

## -see-also

<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitem">IOfflineFilesItem</a>



<a href="/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesitemcontainer">IOfflineFilesItemContainer</a>
