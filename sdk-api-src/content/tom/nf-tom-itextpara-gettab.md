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

The tab alignment. For more information, see <a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">ITextPara::AddTab</a>. 


### -param ptbLeader

Type: <b>long*</b>

The tab leader-character style. For more information, see <a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">ITextPara::AddTab</a>. 


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




<a href="https://msdn.microsoft.com/e53d8988-6c0f-405f-b9da-04c83ff0ff64">AddTab</a>



<a href="https://msdn.microsoft.com/61899b21-a883-440d-bb2c-0c65b6ae48c0">ClearAllTabs</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/82950caa-4fbc-4f80-aae4-91feecccef65">DeleteTab</a>



<a href="https://msdn.microsoft.com/1fb072d7-6311-4a44-b1e1-ec6ee9ba654d">GetListTab</a>



<a href="https://msdn.microsoft.com/4440ce51-f504-4489-851f-08895b23a22b">GetTabCount</a>



<a href="https://msdn.microsoft.com/151d66eb-1bfd-4800-be45-5942ef11d0b8">ITextPara</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/21966279-d84f-4f1a-9e90-5e0e79b14c7e">SetListTab</a>



<a href="https://msdn.microsoft.com/a15f0334-1a31-4bc3-bc1e-e5cf53112007">Text Object Model</a>
 

 

