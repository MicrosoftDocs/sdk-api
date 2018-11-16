---
UID: NF:directxmath.XMComparisonAnyTrue
title: XMComparisonAnyTrue function
author: windows-sdk-content
description: Tests the comparison value to determine if any of the compared components are true.
old-location: dxmath\xmcomparisonanytrue.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMComparisonAnyTrue(uint32_t)
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: Use DirectX..XMComparisonAnyTrue, XMComparisonAnyTrue, XMComparisonAnyTrue method [DirectX Math Support APIs], dxmath.xmcomparisonanytrue
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: directxmath.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: Use DirectX.
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectXMath.h
api_name:
 - XMComparisonAnyTrue
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMComparisonAnyTrue
: 
---

# XMComparisonAnyTrue function


## -description


Tests the comparison value to determine if any of the compared components are true.


## -parameters




### -param CR [in]

Comparison value to test. The comparison value is typically retrieved using a recording version of an DirectXMath
        function such as <a href="https://msdn.microsoft.com/en-us/library/Ee420961(v=VS.85).aspx">XMVector4EqualR</a>. The names of the recording functions
        end with an "R".


## -returns



Returns true if any of the compared components are true.




## -remarks



The following code snippet highlights how this function might be used:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>uint32_t comparisonValue = XMVector4EqualR( V1, V2 );
if( XMComparisonAnyTrue( comparisonValue ) )
{
	DoStuff();
}</pre>
</td>
</tr>
</table></span></div>
The <code>DoStuff</code> function will be called only if any of the four components of <i>V1</i> and <i>V2</i> are
   equal (any compared components are true).

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/4d46fd96-55ca-cb66-f878-caf7894535ae">DirectXMath Library Utility Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437885(v=VS.85).aspx">XMComparisonAllFalse</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437886(v=VS.85).aspx">XMComparisonAllInBounds</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437887(v=VS.85).aspx">XMComparisonAllTrue</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437889(v=VS.85).aspx">XMComparisonAnyFalse</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437893(v=VS.85).aspx">XMComparisonAnyOutOfBounds</a>



<a href="https://msdn.microsoft.com/en-us/library/Hh437908(v=VS.85).aspx">XMComparisonMixed</a>
 

 

