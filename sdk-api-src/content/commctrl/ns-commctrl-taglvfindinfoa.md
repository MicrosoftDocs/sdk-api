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

# tagLVFINDINFOA structure


## -description


Contains information used when searching for a list-view item. This structure is identical to LV_FINDINFO but has been renamed to fit standard naming conventions. 


## -struct-fields




### -field flags

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Type of search to perform. This member can be set to one or more of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="LVFI_PARAM"></a><a id="lvfi_param"></a><dl>
<dt><b>LVFI_PARAM</b></dt>
</dl>
</td>
<td width="60%">
Searches for a match between this structure's <b>lParam</b> member and the <b>lParam</b> member of an item's <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure.

</td>
</tr>
<tr>
<td width="40%"><a id="LVFI_PARTIAL"></a><a id="lvfi_partial"></a><dl>
<dt><b>LVFI_PARTIAL</b></dt>
</dl>
</td>
<td width="60%">
Checks to see if the item text begins with the string pointed to by the <b>psz</b> member. This value implies use of LVFI_STRING.

</td>
</tr>
<tr>
<td width="40%"><a id="LVFI_STRING"></a><a id="lvfi_string"></a><dl>
<dt><b>LVFI_STRING</b></dt>
</dl>
</td>
<td width="60%">
Searches based on the item text. Unless additional values are specified, the item text of the matching item must exactly match the string pointed to by the <b>psz</b> member. However, the search is case-insensitive.

</td>
</tr>
<tr>
<td width="40%"><a id="LVFI_SUBSTRING"></a><a id="lvfi_substring"></a><dl>
<dt><b>LVFI_SUBSTRING</b></dt>
</dl>
</td>
<td width="60%">
<b>Windows Vista and later.</b> Equivalent to LVFI_PARTIAL.

</td>
</tr>
<tr>
<td width="40%"><a id="LVFI_WRAP"></a><a id="lvfi_wrap"></a><dl>
<dt><b>LVFI_WRAP</b></dt>
</dl>
</td>
<td width="60%">
Continues the search at the beginning if no match is found. If this flag is used by itself, it is assumed that a string search is wanted.

</td>
</tr>
<tr>
<td width="40%"><a id="LVFI_NEARESTXY"></a><a id="lvfi_nearestxy"></a><dl>
<dt><b>LVFI_NEARESTXY</b></dt>
</dl>
</td>
<td width="60%">
Finds the item nearest to the position specified in the <b>pt</b> member, in the direction specified by the <b>vkDirection</b> member. This flag is supported only by large icon and small icon modes. If LVFI_NEARESTXY is specified, all other flags are ignored.

</td>
</tr>
</table>
 


### -field psz

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPCTSTR</a></b>

Address of a null-terminated string to compare with the item text. It is valid only if LVFI_STRING or LVFI_PARTIAL is set in the <b>flags</b> member.


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Value to compare with the <b>lParam</b> member of a list-view item's <a href="https://msdn.microsoft.com/4141a2ee-9016-4d76-8758-a36fc6eedb44">LVITEM</a> structure. It is valid only if LVFI_PARAM is set in the <b>flags</b> member.


### -field pt

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a></b>


<a href="https://msdn.microsoft.com/library/windows/hardware/ff569161">POINT</a> structure with the initial search position. It is valid only if LVFI_NEARESTXY is set in the <b>flags</b> member.


### -field vkDirection

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Virtual key code that specifies the direction to search. The following codes are supported: 
			
            		

<ul>
<li>VK_LEFT </li>
<li>VK_RIGHT </li>
<li>VK_UP </li>
<li>VK_DOWN </li>
<li>VK_HOME </li>
<li>VK_END </li>
<li>VK_PRIOR </li>
<li>VK_NEXT </li>
</ul>

                    
                    This member is valid only if LVFI_NEARESTXY is set in the <b>flags</b> member.

