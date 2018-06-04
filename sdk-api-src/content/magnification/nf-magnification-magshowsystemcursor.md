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

# MagShowSystemCursor function


## -description


Shows or hides the system cursor.


## -parameters




### -param fShowCursor [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

TRUE to show the system cursor, or FALSE to hide it.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns TRUE if successful, or FALSE otherwise.




## -remarks



This function does not associate a reference count with the visibility state of the system cursor. Instead, the specified visibility state takes effect immediately, regardless of any previous calls to <b>MagShowSystemCursor</b>.


The system cursor is always magnified when it is shown while the full-screen magnifier is active. 

When used with a magnifier control, calls to <b>MagShowSystemCursor</b> have no effect on the magnified system cursor. The visibility of the magnified system cursor depends on whether the magnifier control has the <a href="magapi_magnifier_styles.htm">MS_SHOWMAGNIFIEDCURSOR</a> style. If it has this style, the magnifier control displays the magnified system cursor, along with the magnified screen content, whenever the system cursor enters the source rectangle.


#### Examples

The following example uses the <b>MagShowSystemCursor</b> function to set the visibility state of the system cursor.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Description:
//   Show or hide the system cursor.
//
// Parameters:
//   fShow - TRUE to show the system cursor, FALSE to hide it.
//
BOOL ShowSystemCursor(BOOL fShow)
{
    BOOL fResult = MagShowSystemCursor(fShow);

    return fResult;
}
</pre>
</td>
</tr>
</table></span></div>


