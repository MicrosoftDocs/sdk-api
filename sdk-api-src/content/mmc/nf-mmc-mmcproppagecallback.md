---
UID: NF:mmc.MMCPropPageCallback
title: MMCPropPageCallback function
author: windows-sdk-content
description: The MMCPropPageCallback function is only required by Microsoft Foundation Classes (MFC)-based snap-ins. The function sets the correct module state during page creation.
old-location: mmc\mmcproppagecallback.htm
tech.root: mmc
ms.assetid: c1f952c5-df0f-4cc5-8d20-66a3a6701060
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: MMCPropPageCallback, MMCPropPageCallback callback, MMCPropPageCallback callback function [MMC], _slate_mmcproppagecallback, mmc.mmcproppagecallback, mmc/MMCPropPageCallback
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: mmc.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Mmc.h
api_name:
 - MMCPropPageCallback
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- MMCPropPageCallback
: 
---

# MMCPropPageCallback function


## -description


The 
<b>MMCPropPageCallback</b> function is only required by Microsoft Foundation Classes (MFC)-based snap-ins. The function sets the correct module state during page creation.


## -parameters




### -param vpsp

A pointer to the Microsoft Windows 
<a href="https://msdn.microsoft.com/en-us/library/Bb774548(v=VS.85).aspx">PROPSHEETPAGE</a> structure. Be aware that by default, MFC installs its own callback in the <b>pfnCallback</b> member of the structure.


## -returns



This callback function can return one of these values.




## -remarks



This function should not be called by snap-ins that statically link MFC libraries. A call to this function by such a snap-in will not link correctly.

For each page derived from <b>CPropertyPage</b>, call 
<b>MMCPropPageCallback</b> with a pointer to the page's callback, following these guidelines:

<ul>
<li>All pages for a particular property sheet must use the same callback pointer.</li>
<li>If you replace MFC's callback with your own, your callback must call MFC's callback.</li>
<li>You must call this function with each <b>CPropertyPage</b> derived class.</li>
</ul>
MFC must have the correct module state set from exported functions or COM interfaces. This includes calls made from the operating system to the module. For exported functions or COM interfaces, this is done by adding the AFX_MANAGE_STATE macro at the beginning of all the exported functions in snap-in DLLs that dynamically link to MFC. This is done by adding the following line of code to the beginning of functions exported from the snap-in:

<div class="code"><span codelanguage="VisualBasic"><table>
<tr>
<th>VB</th>
</tr>
<tr>
<td>
<pre>AFX_MANAGE_STATE(AfxGetStaticModuleState( ))</pre>
</td>
</tr>
</table></span></div>
For an operating system call, MFC does this automatically. Because MMC's property sheet is not an MFC <b>CPropertySheet</b>, the operating system call due to the callback is in the wrong module state. As a result, you need to make sure that the module state is correctly set during the page creation. This is the purpose of 
<b>MMCPropPageCallback</b>. After the module state has been set, the only AFX_MANAGE_STATE calls that need to be made are those exposed by the COM interfaces implemented by the snap-in (for example 
<a href="https://msdn.microsoft.com/14c4f088-ad94-48a1-8c6d-a199b2938074">IExtendPropertySheet2::CreatePropertyPages</a>). To determine whether the application has the correct module state, look at <b>CWinApp</b> and note the application name.




## -see-also




<a href="https://msdn.microsoft.com/28cbf3df-f345-4b4f-ac34-e32e63c9b6ec">PROPSHEETPAGE</a>
 

 

