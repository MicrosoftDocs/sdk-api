---
UID: NF:mswmdm.IWMDMStorage4.GetParent
title: IWMDMStorage4::GetParent
author: windows-sdk-content
description: The GetParent method retrieves the parent of the storage.
old-location: wmdm\iwmdmstorage4_getparent.htm
old-project: WMDM
ms.assetid: e3281501-ec4b-4437-b462-d5b0fd1ac4e0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: GetParent, GetParent method [windows Media Device Manager], GetParent method [windows Media Device Manager],IWMDMStorage4 interface, IWMDMStorage4 interface [windows Media Device Manager],GetParent method, IWMDMStorage4.GetParent, IWMDMStorage4::GetParent, IWMDMStorage4GetParent, mswmdm/IWMDMStorage4::GetParent, wmdm.iwmdmstorage4_getparent
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mswmdm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.typenames: MSVidCtlStateList
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mssachlp.lib
 - mssachlp.dll
api_name:
 - IWMDMStorage4.GetParent
product: Windows
targetos: Windows
req.lib: Mssachlp.lib
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IWMDMStorage4::GetParent


## -description



The <b>GetParent</b> method retrieves the parent of the storage.




## -parameters




### -param ppStorage [out]

Pointer to the <a href="https://msdn.microsoft.com/1ede7c68-0169-4375-9b45-b0995ad14e44">IWMDMStorage</a> interface of the parent storage. The caller must release this interface when finished with it.


## -returns



The method returns an <b>HRESULT</b>. All the interface methods in Windows Media Device Manager can return any of the following classes of error codes:

<ul>
<li>Standard COM error codes </li>
<li>Windows error codes converted to HRESULT values </li>
<li>Windows Media Device Manager error codes </li>
</ul>
For an extensive list of possible error codes, see <a href="https://msdn.microsoft.com/library/windows/hardware/dn938542">Error Codes</a>.




## -remarks



The application can navigate up the storage hierarchy by calling <b>GetParent</b> recursively. After the root storage is reached, <b>GetParent</b> returns S_FALSE and sets <i>ppStorage</i> to <b>NULL</b>.


#### Examples

The following C++ function traverses up to the root parent of a storage.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
HRESULT BubbleUp(IWMDMStorage *pIStorage)
{
    HRESULT hr = S_OK;
    CComPtr&lt;IWMDMStorage4&gt; pStorage4;

    hr = pIStorage-&gt;QueryInterface (__uuidof(IWMDMStorage4), reinterpret_cast&lt;void**&gt;(&amp;pStorage4));
    if (SUCCEEDED(hr))
    {
        while ((pStorage4 != NULL))
        {
            CComPtr&lt;IWMDMStorage&gt; pParent;
            hr = pStorage4-&gt;GetParent(&amp;pParent);
            if (FAILED(hr))
            {
                break;
            }

            //
            // Do something with pParent....
            //
            
            if (S_FALSE != hr)
            {
                hr = pParent-&gt;QueryInterface (__uuidof(IMDSPStorage4), reinterpret_cast&lt;void**&gt;(&amp;pStorage4));
                if (FAILED(hr))
                {
                    break;
                }
            }
        } // Loop up to next parent.
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/ac80cc08-0ff0-48ee-b9c6-e094f803b751">IWMDMStorage4 Interface</a>
 

 

