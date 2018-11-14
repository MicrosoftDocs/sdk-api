---
UID: NF:winsync.ISynchronousDataRetriever.LoadChangeData
title: ISynchronousDataRetriever::LoadChangeData
author: windows-sdk-content
description: Retrieves item data for a change.
old-location: winsync\isynchronousdataretriever_loadchangedata.htm
tech.root: winsync
ms.assetid: ae309301-3810-4785-b4f2-a55fbdf819d8
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: ISynchronousDataRetriever interface [Windows Sync],LoadChangeData method, ISynchronousDataRetriever.LoadChangeData, ISynchronousDataRetriever::LoadChangeData, LoadChangeData, LoadChangeData method [Windows Sync], LoadChangeData method [Windows Sync],ISynchronousDataRetriever interface, winsync.isynchronousdataretriever_loadchangedata, winsync/ISynchronousDataRetriever::LoadChangeData
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - ISynchronousDataRetriever.LoadChangeData
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- winsync.h
: 
- ISynchronousDataRetriever.LoadChangeData
: 
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

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CItemStore::LoadChangeData(
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
        hr = pLoadChangeContext-&gt;GetSyncChange(&amp;pChange);
        if (SUCCEEDED(hr))
        {
            SYNC_GID gidItem;
            DWORD cbID = sizeof(gidItem);
            hr = pChange-&gt;GetRootItemId((BYTE*)&amp;gidItem, &amp;cbID);
            if (SUCCEEDED(hr))
            {
                IXMLDOMNode* pNodeItem = NULL;
                hr = FindItem(&amp;gidItem, &amp;pNodeItem);
                if (SUCCEEDED(hr))
                {
                    IXMLDOMNode* pNodeClone = NULL;
                    hr = pNodeItem-&gt;cloneNode(TRUE, &amp;pNodeClone);
                    if (SUCCEEDED(hr))
                    {
                        hr = pNodeClone-&gt;QueryInterface(IID_IUnknown, (void**)ppUnkData);

                        pNodeClone-&gt;Release();
                    }

                    pNodeItem-&gt;Release();                
                }
            }

            pChange-&gt;Release();
        }
    }

    return hr;
}</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/11d8971b-354f-4347-9d3f-6d32df8dc9d2">ILoadChangeContext Interface</a>



<a href="https://msdn.microsoft.com/d59a5198-5878-4a48-b6c4-042afc36054d">ISynchronousDataRetriever Interface</a>
 

 

