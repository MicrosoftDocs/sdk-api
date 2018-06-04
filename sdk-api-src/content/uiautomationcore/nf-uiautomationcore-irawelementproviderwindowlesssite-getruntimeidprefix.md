---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# IRawElementProviderWindowlessSite::GetRuntimeIdPrefix


## -description


Retrieves a Microsoft UI Automation runtime ID that is unique to the windowless Microsoft ActiveX control site. 


## -parameters




### -param pRetVal






#### - ppRetVal [out, retval]

Type: <b><a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a>**</b>

Receives the runtime ID.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A UI Automation fragment must implement the <a href="https://msdn.microsoft.com/e1252353-235e-489e-8eb9-be80d4850ca4">IRawElementProviderFragment::GetRuntimeId</a> method to return a unique ID for the fragment.  This is difficult for a windowless ActiveX control, which must be able to identify itself as unique among other windowless controls in the ActiveX control container.  To resolve this issue, the windowless site should implement the <b>GetRuntimeIdPrefix</b>  method by forming a <a href="http://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> that contains the constant <b>UiaAppendRuntimeId</b>, followed by an integer value that is unique to this windowless site.  

The fragment can then append an integer value that is unique relative to all other fragments in the windowless ActiveX control, and return it to the client.  



For example, the site might return a SAFEARRAY with the following contents: <code>{ UiaAppendRuntimeId, 3 }</code>.  This might represent the third ActiveX control in the container.  The fragment provider's <a href="https://msdn.microsoft.com/e1252353-235e-489e-8eb9-be80d4850ca4">GetRuntimeId</a> method could then form a SAFEARRAY with the following contents: <code>{ UiaAppendRuntimeId, 3, 5 }</code>.  This might represent the fifth fragment within the ActiveX container.  The whole SAFEARRAY would be a unique ID relative to the whole ActiveX control container.



A provider typically calls this method as part of handling the <a href="https://msdn.microsoft.com/e1252353-235e-489e-8eb9-be80d4850ca4">GetRuntimeId</a> method.


#### Examples

The following C++ code example shows how to implement the <b>GetRuntimeIdPrefix</b> method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>IFACEMETHODIMP CProviderWindowlessSite::GetRuntimeIdPrefix(   
     SAFEARRAY **ppsaPrefix)   
{   
    if (ppsaPrefix == NULL) 
    {
        return E_INVALIDARG;
    }

    // m_siteIndex is the index of the windowless control's
    // site. It is defined by the control container.
    int rId[] = { UiaAppendRuntimeId, m_siteIndex };
    SAFEARRAY *psa = SafeArrayCreateVector(VT_I4, 0, 2);  
    if (psa == NULL)
    {
        return E_OUTOFMEMORY;
    }

    for (LONG i = 0; i &lt; 2; i++)
    {
        SafeArrayPutElement(psa, &amp;i, (void*)&amp;(rId[i]));
    }

    *ppsaPrefix = psa;  
    return S_OK;  
}  
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/E6BE069B-C639-4578-9E5F-8CFE1267A847">IRawElementProviderWindowlessSite</a>
 

 

