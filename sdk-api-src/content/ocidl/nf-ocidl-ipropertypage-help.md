---
UID: NF:ocidl.IPropertyPage.Help
title: IPropertyPage::Help (ocidl.h)
author: windows-sdk-content
description: Invokes the property page help in response to an end-user request.
old-location: com\ipropertypage_help.htm
tech.root: com
ms.assetid: ba715518-1aa0-42de-bad7-f2d0d0f00460
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Help, Help method [COM], Help method [COM],IPropertyPage interface, IPropertyPage interface [COM],Help method, IPropertyPage.Help, IPropertyPage::Help, _ctrl_ipropertypage_help, com.ipropertypage_help, ocidl/IPropertyPage::Help
ms.topic: method
f1_keywords: 
 - "ocidl/IPropertyPage.Help"
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - OCIdl.h
api_name:
 - IPropertyPage.Help
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyPage::Help


## -description


Invokes the property page help in response to an end-user request.


## -parameters




### -param pszHelpDir [in]

A pointer to the string under the <b>HelpDir</b> key in the property page's CLSID information in the registry. If <b>HelpDir</b> does not exist, this will be the path found in the <b><a href="https://docs.microsoft.com/windows/desktop/com/inprocserver32">InprocServer32</a></b> entry minus the server file name. (Note that <b><a href="https://docs.microsoft.com/windows/desktop/com/localserver32">LocalServer32</a></b> is not checked, because local property pages are not supported).


## -returns



This method can return the standard return values E_OUTOFMEMORY and E_UNEXPECTED, as well as the following values.

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
The page displayed its own help.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Help is either not provided or is provided only through the information is <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/ns-ocidl-tagproppageinfo">PROPPAGEINFO</a>.

</td>
</tr>
</table>
 




## -remarks



<h3><a id="Notes_to_Callers"></a><a id="notes_to_callers"></a><a id="NOTES_TO_CALLERS"></a>Notes to Callers</h3>
Calls to this method must occur between calls to <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-activate">IPropertyPage::Activate</a> and <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-deactivate">IPropertyPage::Deactivate</a>.

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
If the page fails this method (such as E_NOTIMPL), then the frame will attempt to use the <b>pszHelpFile</b> and <b>dwHelpContext</b> members of the <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/ns-ocidl-tagproppageinfo">PROPPAGEINFO</a> structure obtained through <a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nf-ocidl-ipropertypage-getpageinfo">IPropertyPage::GetPageInfo</a>. Therefore, the page should either implement <b>IPropertyPage::Help</b> or return help information through <b>IPropertyPage::GetPageInfo</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/nn-ocidl-ipropertypage">IPropertyPage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/ocidl/ns-ocidl-tagproppageinfo">PROPPAGEINFO</a>
 

 

