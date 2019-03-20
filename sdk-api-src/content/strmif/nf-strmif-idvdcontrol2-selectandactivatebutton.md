---
UID: NF:strmif.IDvdControl2.SelectAndActivateButton
title: IDvdControl2::SelectAndActivateButton (strmif.h)
author: windows-sdk-content
description: The SelectAndActivateButton method selects and activates the specified menu button.
old-location: dshow\idvdcontrol2_selectandactivatebutton.htm
tech.root: DirectShow
ms.assetid: 1e5ad753-bc35-4a98-83d8-82ffccbbe3ed
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDvdControl2 interface [DirectShow],SelectAndActivateButton method, IDvdControl2.SelectAndActivateButton, IDvdControl2::SelectAndActivateButton, IDvdControl2SelectAndActivateButton, SelectAndActivateButton, SelectAndActivateButton method [DirectShow], SelectAndActivateButton method [DirectShow],IDvdControl2 interface, dshow.idvdcontrol2_selectandactivatebutton, strmif/IDvdControl2::SelectAndActivateButton
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Strmiids.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IDvdControl2.SelectAndActivateButton
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDvdControl2::SelectAndActivateButton


## -description



The <code>SelectAndActivateButton</code> method selects and activates the specified menu button.




## -parameters




### -param ulButton [in]

Value from 1 through 36 that specifies the button to select and activate.


## -returns



Returns one of the following values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>ulButton</i> is out of range.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
The <i>ulButton</i> value is valid, but the <a href="https://msdn.microsoft.com/3b2c01a2-d52c-4497-8fc9-d1113e8507e8">DVD Navigator</a> filter couldn't activate it.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VFW_E_DVD_OPERATION_INHIBITED</b></dt>
</dl>
</td>
<td width="60%">
UOP control prohibits the operation.

</td>
</tr>
</table>
 




## -remarks



The following table shows the Annex J command name to which this method name corresponds, and the domains in which this method is valid.

<table>
<tr>
<td>Annex J Command Name
            </td>
<td>Valid Domains
            </td>
</tr>
<tr>
<td>Button_Select_and_Activate</td>
<td>
<ul>
<li>DVD_DOMAIN_VideoManagerMenu</li>
<li>DVD_DOMAIN_VideoTitleSetMenu</li>
<li>DVD_DOMAIN_Title</li>
</ul>
</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6f41e0f1-e550-4ca6-9a80-ce4d498289e2">DVD Applications</a>



<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/eda43b20-1c4d-4769-bb87-3942716af13c">IDvdControl2 Interface</a>



<a href="https://msdn.microsoft.com/8c5f8072-b74f-4e15-8991-73bcc4145fd2">Working With DVD Menus</a>
 

 

