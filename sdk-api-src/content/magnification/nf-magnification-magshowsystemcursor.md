---
UID: NF:magnification.MagShowSystemCursor
title: MagShowSystemCursor function
author: windows-sdk-content
description: Shows or hides the system cursor.
old-location: magapi\magapi_magshowsystemcursor.htm
old-project: magapi
ms.assetid: 0C4D92D8-9B06-4592-A0FF-8AE4378E5641
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MagShowSystemCursor, MagShowSystemCursor function [Magnification API], magapi.magapi_magshowsystemcursor, magnification/MagShowSystemCursor
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: magnification.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: MCAST_SCOPE_ENTRY, *PMCAST_SCOPE_ENTRY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagShowSystemCursor
product: Windows
targetos: Windows
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
req.product: GDI+ 1.1
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


