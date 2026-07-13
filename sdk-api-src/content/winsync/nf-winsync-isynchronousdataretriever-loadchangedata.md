---
UID: NF:winsync.ISynchronousDataRetriever.LoadChangeData
title: ISynchronousDataRetriever::LoadChangeData (winsync.h)
description: Retrieves item data for a change. (ISynchronousDataRetriever.LoadChangeData)
helpviewer_keywords: ["ISynchronousDataRetriever interface [Windows Sync]","LoadChangeData method","ISynchronousDataRetriever.LoadChangeData","ISynchronousDataRetriever::LoadChangeData","LoadChangeData","LoadChangeData method [Windows Sync]","LoadChangeData method [Windows Sync]","ISynchronousDataRetriever interface","winsync.isynchronousdataretriever_loadchangedata","winsync/ISynchronousDataRetriever::LoadChangeData"]
old-location: winsync\isynchronousdataretriever_loadchangedata.htm
tech.root: winsync
ms.assetid: ae309301-3810-4785-b4f2-a55fbdf819d8
ms.date: 12/05/2018
ms.keywords: ISynchronousDataRetriever interface [Windows Sync],LoadChangeData method, ISynchronousDataRetriever.LoadChangeData, ISynchronousDataRetriever::LoadChangeData, LoadChangeData, LoadChangeData method [Windows Sync], LoadChangeData method [Windows Sync],ISynchronousDataRetriever interface, winsync.isynchronousdataretriever_loadchangedata, winsync/ISynchronousDataRetriever::LoadChangeData
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISynchronousDataRetriever::LoadChangeData
 - winsync/ISynchronousDataRetriever::LoadChangeData
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISynchronousDataRetriever.LoadChangeData
---

# ISynchronousDataRetriever::LoadChangeData


## -description

Retrieves item data for a change.

## -parameters

### -param pLoadChangeContext [in]

Metadata that describes the change for which data should be retrieved.

### -param ppUnkData [out]

Returns the item data for the change specified in <i>pLoadChangeContext</i>.

## -returns

The possible return codes include, but are not limited to, the values shown in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Provider-determined error codes.</b></dt>
</dl>
</td>
<td width="60%"></td>
</tr>
</table>

## -remarks

The source provider determines the data retrieval interface that is implemented by the object that is returned in <i>ppUnkData</i>. The destination provider can acquire this interface by using the <b>QueryInterface</b> method of <i>ppUnkData</i>.


#### Examples

The following example is an implementation of <b>LoadChangeData</b> that finds the specified change in a custom data store and returns a copy of it.


```cpp
STDMETHODIMP CItemStore::LoadChangeData(
    ILoadChangeContext * pLoadChangeContext,
    IUnknown ** ppUnkData)
{
    HRESULT hr = E_UNEXPECTED;

    if (NULL == pLoadChangeContext || NULL == ppUnkData)
    {
        hr = E_POINTER;    
    }
    else
    {
        // Find the item in the data store, clone it, and return its IUnknown interface.
        ISyncChange* pChange = NULL;
        hr = pLoadChangeContext->GetSyncChange(&pChange);
        if (SUCCEEDED(hr))
        {
            SYNC_GID gidItem;
            DWORD cbID = sizeof(gidItem);
            hr = pChange->GetRootItemId((BYTE*)&gidItem, &cbID);
            if (SUCCEEDED(hr))
            {
                IXMLDOMNode* pNodeItem = NULL;
                hr = FindItem(&gidItem, &pNodeItem);
                if (SUCCEEDED(hr))
                {
                    IXMLDOMNode* pNodeClone = NULL;
                    hr = pNodeItem->cloneNode(TRUE, &pNodeClone);
                    if (SUCCEEDED(hr))
                    {
                        hr = pNodeClone->QueryInterface(IID_IUnknown, (void**)ppUnkData);

                        pNodeClone->Release();
                    }

                    pNodeItem->Release();                
                }
            }

            pChange->Release();
        }
    }

    return hr;
}
```

## -see-also

<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-iloadchangecontext">ILoadChangeContext Interface</a>



<a href="/previous-versions/windows/desktop/api/winsync/nn-winsync-isynchronousdataretriever">ISynchronousDataRetriever Interface</a>
