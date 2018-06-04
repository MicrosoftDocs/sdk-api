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

# IWizardExtension::AddPages


## -description


Adds extension pages to the wizard by filling an array with handles to <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> structures representing those pages.


## -parameters




### -param aPages [out]

Type: <b>HPROPSHEETPAGE*</b>

A pointer to an array of <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> handles that represent the wizard dialog pages. Handles to <b>PROPSHEETPAGE</b> structures for the extension pages are added to this array.


### -param cPages [in]

Type: <b>UINT</b>

The count of elements in <i>aPages</i>.


### -param pnPagesAdded [out]

Type: <b>UINT*</b>

The count of handles successfully added.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The array of handles pointed to by <i>aPages</i> can contain handles to wizard dialog pages preceding and following the extension pages. The array's pointer should be passed to this method so that its value is the first empty array element, ready to accept the handle of the first extension page, rather than simply the first element. Collaterally, the value passed in <i>cPages</i> should state the number of unused array elements instead of the total number.

For example, if two introductory host pages were added to an array called <b>hpages</b>, then the call to <b>IWizardExtension::AddPages</b> would appear as follows.

				

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>#define ARRAYSIZE(a)    (sizeof(a)/sizeof(a[0]))
g_iwe-&gt;AddPages(&amp;hpages[2], ARRAYSIZE(hpages)-2, &amp;nPages);</pre>
</td>
</tr>
</table></span></div>
Do not confuse wizard pages, which are <a href="https://msdn.microsoft.com/69ceb9f4-f68c-4c60-9610-4c1977aae4b8">PROPSHEETPAGE</a> structures, with hosted HTML pages. One wizard dialog page can host many sequential HTML pages. This method supplies the number of wizard dialog pages added by the wizard extension, not the number of server-side HTML pages which are displayed in it.



