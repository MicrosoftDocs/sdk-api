---
UID: NF:tom.ITextPara.GetTab
title: ITextPara::GetTab
author: windows-sdk-content
description: Retrieves tab parameters (displacement, alignment, and leader style) for a specified tab.
old-location: controls\ITextPara_GetTab.htm
old-project: controls
ms.assetid: VS|Controls|~\controls\richedit\textobjectmodel\textobjectmodelreference\textobjectmodelinterfaces\gettab.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetTab, GetTab method [Windows Controls], GetTab method [Windows Controls],ITextPara interface, ITextPara interface [Windows Controls],GetTab method, ITextPara.GetTab, ITextPara::GetTab, _win32_ITextPara_GetTab, _win32_ITextPara_GetTab_cpp, controls.ITextPara_GetTab, controls._win32_ITextPara_GetTab, tom/ITextPara::GetTab
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
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
tech.root: 
req.typenames: MANCODE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msftedit.dll
api_name:
 - ITextPara.GetTab
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextPara::GetTab


## -description


Retrieves tab parameters (displacement, alignment, and leader style) for a specified tab. 


## -parameters




### -param iTab

Type: <b>long</b>

Index of tab for which to retrieve info. It can be either a numerical index or a special value (see the following table). Since tab indexes are zero-based, <i>iTab</i> = zero gets the first tab defined, <i>iTab</i> = 1 gets the second tab defined, and so forth. The following table summarizes all of the possible values of <i>iTab</i>. 
					

<table class="clsStd">
<tr>
<th><i>iTab</i></th>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td>tomTabBack</td>
<td>–3</td>
<td>Get tab previous to * <i>ptbPos</i></td>
</tr>
<tr>
<td>tomTabNext</td>
<td>–2</td>
<td>Get tab following * <i>ptbPos</i></td>
</tr>
<tr>
<td>tomTabHere </td>
<td>–1</td>
<td>Get tab at * <i>ptbPos</i></td>
</tr>
<tr>
<td></td>
<td>&gt;= 0</td>
<td>Get tab with index of <i>iTab</i> (and ignore <i>ptbPos</i>).</td>
</tr>
</table>
 


### -param ptbPos

Type: <b>float*</b>

The tab displacement, in floating-point points. The value of * <i>ptbPos</i> is zero if the tab does not exist and the value of * <i>ptbPos</i> is tomUndefined if there are multiple values in the associated range. 


### -param ptbAlign

Type: <b>long*</b>

The tab alignment. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb787728(v=VS.85).aspx">ITextPara::AddTab</a>. 


### -param ptbLeader

Type: <b>long*</b>

The tab leader-character style. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Bb787728(v=VS.85).aspx">ITextPara::AddTab</a>. 


## -returns



Type: <b>HRESULT</b>

If <b>ITextPara::GetTab</b> succeeds, it returns <b>S_OK</b>. If the method fails, it returns one of the following COM error codes. For more information about COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>Value</b></dt>
</dl>
</td>
<td width="60%">
Meaning

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_RELEASED</b></dt>
</dl>
</td>
<td width="60%">
The paragraph formatting object is attached to a range that has been deleted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There is no tab corresponding to iTab.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb787728(v=VS.85).aspx">AddTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787738(v=VS.85).aspx">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb787748(v=VS.85).aspx">DeleteTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb773989(v=VS.85).aspx">GetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774035(v=VS.85).aspx">GetTabCount</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb774056(v=VS.85).aspx">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/en-us/library/Bb774177(v=VS.85).aspx">SetListTab</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb787607(v=VS.85).aspx">Text Object Model</a>
 

 

