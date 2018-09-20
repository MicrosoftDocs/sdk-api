---
UID: NF:uiautomationcore.IRawElementProviderWindowlessSite.GetRuntimeIdPrefix
title: IRawElementProviderWindowlessSite::GetRuntimeIdPrefix
author: windows-sdk-content
description: Retrieves a Microsoft UI Automation runtime ID that is unique to the windowless Microsoft ActiveX control site.
old-location: winauto\uiauto_IRawElementProviderWindowlessSite_getRuntimeIdPrefix.htm
tech.root: WinAuto
ms.assetid: E10BBE53-5AAB-4BAB-AFC8-866224011E43
ms.author: windowssdkdev
ms.date: 09/19/2018
ms.keywords: GetRuntimeIdPrefix, GetRuntimeIdPrefix method [Windows Accessibility], GetRuntimeIdPrefix method [Windows Accessibility],IRawElementProviderWindowlessSite interface, IRawElementProviderWindowlessSite interface [Windows Accessibility],GetRuntimeIdPrefix method, IRawElementProviderWindowlessSite.GetRuntimeIdPrefix, IRawElementProviderWindowlessSite::GetRuntimeIdPrefix, uiautomationcore/IRawElementProviderWindowlessSite::GetRuntimeIdPrefix, winauto.uiauto_IRawElementProviderWindowlessSite_getRuntimeIdPrefix
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
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
 - UIAutomationCore.h
api_name:
 - IRawElementProviderWindowlessSite.GetRuntimeIdPrefix
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IRawElementProviderWindowlessSite::GetRuntimeIdPrefix


## -description


Retrieves a Microsoft UI Automation runtime ID that is unique to the windowless Microsoft ActiveX control site. 


## -parameters




### -param pRetVal

TBD




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
 

 

