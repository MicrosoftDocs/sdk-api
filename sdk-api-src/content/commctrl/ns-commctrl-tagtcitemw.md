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

# tagTCITEMW structure


## -description


Specifies or receives the attributes of a tab item. It is used with the <a href="https://msdn.microsoft.com/e547c49a-699c-4137-8680-20391d138d54">TCM_INSERTITEM</a>, <a href="https://msdn.microsoft.com/41774f14-c4e9-4c98-bc25-3522b2125ed5">TCM_GETITEM</a>, and <a href="https://msdn.microsoft.com/1d9c6607-d8ec-4644-a714-22bc2677aa78">TCM_SETITEM</a> messages. This structure supersedes the 
			<b>TC_ITEM</b> structure. 


## -struct-fields




### -field mask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>

Value that specifies which members to retrieve or set. This member can be a combination of the following values: 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TCIF_IMAGE"></a><a id="tcif_image"></a><dl>
<dt><b>TCIF_IMAGE</b></dt>
</dl>
</td>
<td width="60%">
The <b>iImage</b> member is valid. 

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_PARAM"></a><a id="tcif_param"></a><dl>
<dt><b>TCIF_PARAM</b></dt>
</dl>
</td>
<td width="60%">
The  
						<b>lParam</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_RTLREADING"></a><a id="tcif_rtlreading"></a><dl>
<dt><b>TCIF_RTLREADING</b></dt>
</dl>
</td>
<td width="60%">
The string pointed to by 
						<b>pszText</b> will be displayed in the direction opposite to the text in the parent window.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_STATE"></a><a id="tcif_state"></a><dl>
<dt><b>TCIF_STATE</b></dt>
</dl>
</td>
<td width="60%">

<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.70</a>. The 
<b>dwState</b> member is valid.

</td>
</tr>
<tr>
<td width="40%"><a id="TCIF_TEXT"></a><a id="tcif_text"></a><dl>
<dt><b>TCIF_TEXT</b></dt>
</dl>
</td>
<td width="60%">
The <b>pszText</b> member is valid.

</td>
</tr>
</table>
 


### -field dwState

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.70</a>. Specifies the item's current state if information is being retrieved. If item information is being set, this member contains the state value to be set for the item. For a list of valid tab control item states, see <a href="https://msdn.microsoft.com/c4181fe6-0055-45c9-a3d0-8cda051383f2">Tab Control Item States</a>. This member is ignored in the <a href="https://msdn.microsoft.com/e547c49a-699c-4137-8680-20391d138d54">TCM_INSERTITEM</a> message. 


### -field dwStateMask

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.70</a>. Specifies which bits of the <b>dwState</b> member contain valid information. This member is ignored in the <a href="https://msdn.microsoft.com/e547c49a-699c-4137-8680-20391d138d54">TCM_INSERTITEM</a> message. 


### -field pszText

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPTSTR</a></b>

Pointer to a null-terminated string that contains the tab text when item information is being set. If item information is being retrieved, this member specifies the address of the buffer that receives the tab text. 


### -field cchTextMax

Type: <b>int</b>

Size in <b>TCHAR</b><b>s</b> of the buffer pointed to by the 
					<b>pszText</b> member. If the structure is not receiving information, this member is ignored. 


### -field iImage

Type: <b>int</b>

Index in the tab control's image list, or -1 if there is no image for the tab. 


### -field lParam

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LPARAM</a></b>

Application-defined data associated with the tab control item. If more or less than 4 bytes of application-defined data exist per tab, an application must define a structure and use it instead of the <b>TCITEM</b> structure. The first member of the application-defined structure must be a <a href="https://msdn.microsoft.com/018a0de7-fc05-4b56-817b-1af36261fff2">TCITEMHEADER</a> structure. 


#### - lpReserved1

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.00</a>. Not used. 


#### - lpReserved2

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">UINT</a></b>


<a href="https://msdn.microsoft.com/1B524A91-B433-4968-9546-8A6AFB67E89C">Version 4.00</a>. Not used. 


## -remarks



Typically, windows display text left-to-right (LTR). Windows can be 
				<i>mirrored</i> to display languages such as Hebrew or Arabic that read right-to-left (RTL). Ordinarily, <b>pszText</b> will be displayed in the same direction as the text in its parent window. If TCIF_RTLREADING is set, <b>pszText</b> will read in the opposite direction from the text in the parent window.



