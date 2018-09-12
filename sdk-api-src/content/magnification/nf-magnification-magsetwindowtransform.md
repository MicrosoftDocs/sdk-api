---
UID: NF:magnification.MagSetWindowTransform
title: MagSetWindowTransform function
author: windows-sdk-content
description: Sets the transformation matrix for a magnifier control.
old-location: magapi\magapi_MagSetWindowTransform.htm
tech.root: magapi
ms.assetid: VS|magapi|~\magapi\reference\functions\magsetwindowtransform.htm
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: MagSetWindowTransform, MagSetWindowTransform function [Magnification API], magapi.magapi_MagSetWindowTransform, magapi_MagSetWindowTransform, magnification/MagSetWindowTransform
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: magnification.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Magnification.lib
req.dll: Magnification.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Magnification.dll
api_name:
 - MagSetWindowTransform
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# MagSetWindowTransform function


## -description


Sets the transformation matrix for a magnifier control. 


## -parameters




### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The magnification window.


### -param pTransform [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms692385(v=VS.85).aspx">PMAGTRANSFORM</a></b>

A transformation matrix.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">BOOL</a></b>

Returns <b>TRUE</b> if successful, or <b>FALSE</b> otherwise.




## -remarks



The transformation matrix specifies the magnification factor that the magnifier control applies to the contents of the source rectangle.


#### Examples

The following example shows how to set the magnification factor for a magnifier control.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Description:
//   Sets the magnification factor for a magnifier control.
// Parameters:
//   hwndMag - Handle of the magnifier control.
//   magFactor - New magnification factor.
//
BOOL SetMagnificationFactor(HWND hwndMag, float magFactor)
{
    MAGTRANSFORM matrix;
    memset(&amp;matrix, 0, sizeof(matrix));
    matrix.v[0][0] = magFactor;
    matrix.v[1][1] = magFactor;
    matrix.v[2][2] = 1.0f;

    return MagSetWindowTransform(hwndMag, &amp;matrix);  
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms692391(v=VS.85).aspx">MagGetWindowTransform</a>
 

 

