---
UID: NF:shobjidl.IWizardExtension.AddPages
title: IWizardExtension::AddPages
author: windows-driver-content
description: Adds extension pages to the wizard by filling an array with handles to PROPSHEETPAGE structures representing those pages.
old-location: shell\IWizardExtension_AddPages.htm
old-project: shell
ms.assetid: 2d9a5012-3b5e-4e55-984b-70a932bab569
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: AddPages, AddPages method [Windows Shell], AddPages method [Windows Shell],IWizardExtension interface, IWizardExtension interface [Windows Shell],AddPages method, IWizardExtension.AddPages, IWizardExtension::AddPages, _shell_IWizardExtension_AddPages, shell.IWizardExtension_AddPages, shobjidl/IWizardExtension::AddPages
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: shobjidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VPWATERMARKFLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Shell32.dll
api_name:
-	IWizardExtension.AddPages
product: Windows
targetos: Windows
req.lib: 
req.dll: Shell32.dll
req.irql: 
req.product: Internet Explorer 6.01
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



