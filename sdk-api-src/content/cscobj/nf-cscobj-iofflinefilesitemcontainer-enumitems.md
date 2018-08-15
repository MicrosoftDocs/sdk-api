---
UID: NF:cscobj.IOfflineFilesItemContainer.EnumItems
title: IOfflineFilesItemContainer::EnumItems
author: windows-sdk-content
description: Returns an enumerator of child items for the cache item implementing this method.
old-location: of\iofflinefilesitemcontainer_enumitems.htm
old-project: offlinefiles
ms.assetid: 9960e8f8-4d15-4a53-aa77-d0105b6a59d1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: EnumItems, EnumItems method [Offline Files], EnumItems method [Offline Files],IOfflineFilesItemContainer interface, IOfflineFilesItemContainer interface [Offline Files],EnumItems method, IOfflineFilesItemContainer.EnumItems, IOfflineFilesItemContainer::EnumItems, OFFLINEFILES_ITEM_QUERY_CONNECTIONSTATE, OFFLINEFILES_ITEM_QUERY_INCLUDETRANSPARENTCACHE, OFFLINEFILES_ITEM_QUERY_LOCALDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEDIRTYBYTECOUNT, OFFLINEFILES_ITEM_QUERY_REMOTEINFO, cscobj/IOfflineFilesItemContainer::EnumItems, of.iofflinefilesitemcontainer_enumitems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: cscobj.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: OFFLINEFILES_SYNC_STATE
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
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesItemContainer::EnumItems


## -description


Returns an enumerator of child items for the cache item implementing this method. Server, share, and directory entries in the Offline Files cache implement this method to expose the enumeration of their immediate children.
<div class="alert"><b>Note</b>  A call to <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> to query a file item for <b>IID_IOfflineFilesItemContainer</b> fails with <b>E_NOINTERFACE</b>, because file items have no children.</div><div> </div>

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

Enumerator of <a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a> interface pointers.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



To begin a top-down enumeration of the entire cache, perform the following steps:

<ol>
<li>Create an instance of <b>CLSID_OfflineFilesCache</b> and obtain its <a href="https://msdn.microsoft.com/328ad076-cafd-461e-8085-7fca65063fa0">IOfflineFilesItemContainer</a> interface.</li>
<li>Call the <b>EnumItems</b> method to obtain an enumerator for the server entries.</li>
<li>For each entry returned, call <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> for  <a href="https://msdn.microsoft.com/328ad076-cafd-461e-8085-7fca65063fa0">IOfflineFilesItemContainer</a>.</li>
<li>If <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> succeeds, the item supports children.  If so, enumerate each child, calling <b>QueryInterface</b> for <a href="https://msdn.microsoft.com/328ad076-cafd-461e-8085-7fca65063fa0">IOfflineFilesItemContainer</a> on each.  This pattern may be recursively applied to enumerate the entire cache.</li>
</ol>

#### Examples

This example illustrates how to perform a top-down traversal of the Offline Files cache using a simple recursive implementation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT EnumItems(IOfflineFilesItemContainer *pContainer);

//
// Emits the item's path string to the console.
//
HRESULT ReportItem(
    IOfflineFilesItem *pItem
    )
{
    LPWSTR pszPath;
    HRESULT hr = pItem-&gt;GetPath(&amp;pszPath);
    if (SUCCEEDED(hr))
    {
        LPCWSTR pszType = L"";
        OFFLINEFILES_ITEM_TYPE ItemType;
        hr = pItem-&gt;GetItemType(&amp;ItemType);
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
        hr = pItem-&gt;QueryInterface(IID_IOfflineFilesItemContainer,
                                   (void **)&amp;pContainer);
        if (SUCCEEDED(hr))
        {
            EnumItems(pContainer);
            pContainer-&gt;Release();
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
    HRESULT hr = pContainer-&gt;EnumItems(0, &amp;pEnum);
    if (SUCCEEDED(hr))
    {
        IOfflineFilesItem *pItem;
        ULONG celt;
        while(S_OK == (hr = pEnum-&gt;Next(1, &amp;pItem, &amp;celt)))
        {
            ProcessItem(pItem);
            pItem-&gt;Release();
        }
        pEnum-&gt;Release();
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
    HRESULT hr = pCache-&gt;QueryInterface(IID_IOfflineFilesItemContainer,
                                        (void **)&amp;pContainer);
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
                              (void **)&amp;pCache);
        if (SUCCEEDED(hr))
        {
            hr = EnumItemsInCache(pCache);
            pCache-&gt;Release();
        }
        CoUninitialize();
    }
    return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>



<a href="https://msdn.microsoft.com/328ad076-cafd-461e-8085-7fca65063fa0">IOfflineFilesItemContainer</a>
 

 

