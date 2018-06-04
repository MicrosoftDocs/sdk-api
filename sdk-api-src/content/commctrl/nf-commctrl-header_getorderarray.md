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

# Header_GetOrderArray macro


## -description


Gets the current left-to-right order of items in a header control. You can use this macro or send the <a href="https://msdn.microsoft.com/b287d3c1-ae61-41a4-a884-dc008eb24ad8">HDM_GETORDERARRAY</a> message explicitly. 


## -parameters




### -param hwnd

TBD


### -param iCount

TBD


### -param lpi

TBD






#### - hwndHD

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

A handle to a header control. 


#### - iSize

Type: <b>int</b>

The number of integer elements that 
					<i>lpiArray</i> can hold. This value must be equal to the number of items in the control (see <a href="https://msdn.microsoft.com/0e6d2131-53b4-4927-bd0f-577b8eaf237a">HDM_GETITEMCOUNT</a>).


#### - lpiArray

Type: <b>int*</b>

A pointer to an array of integers that receive the index values for items in the header.


## -remarks



The number of elements in <i>lpiArray</i> is specified in <i>iSize</i> and must be equal to the number of items in the control. For example, the following code fragment will reserve enough memory to hold the index values. 

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>
int iItems,

    *lpiArray;



// Get memory for buffer

if((iItems = SendMessage(hwndHD, HDM_GETITEMCOUNT, 0,0))!=-1)

    if(!(lpiArray = calloc(iItems,sizeof(int))))

MessageBox(hwnd, "Out of memory.","Error", MB_OK);</pre>
</td>
</tr>
</table></span></div>


