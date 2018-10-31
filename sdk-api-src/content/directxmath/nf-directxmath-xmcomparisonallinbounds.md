---
UID: NF:directxmath.XMComparisonAllInBounds
title: XMComparisonAllInBounds function
author: windows-sdk-content
description: Tests the comparison value to determine if all of the compared components are within set bounds.
old-location: dxmath\xmcomparisonallinbounds.htm
tech.root: dxmath
ms.assetid: M:Microsoft.directx_sdk.reference.XMComparisonAllInBounds(uint32_t)
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: Use DirectX..XMComparisonAllInBounds, XMComparisonAllInBounds, XMComparisonAllInBounds method [DirectX Math Support APIs], dxmath.xmcomparisonallinbounds
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
 - XMComparisonAllInBounds
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- XMComparisonAllInBounds
: 
---

# XMComparisonAllInBounds function


## -description


Tests the comparison value to determine if all of the compared components are within set bounds.


## -parameters




### -param CR [in]

Comparison value to test. The comparison value is typically retrieved using a recording version of an DirectXMath
        function such as <a href="https://msdn.microsoft.com/a55a4fb4-ff6c-4b50-bc14-9e43c4c1683f">XMVectorInBoundsR</a>. The names of the recording functions end
        with an "R".


## -returns



Returns true if all of the compared components within the set bounds.




## -remarks



The following code snippet highlights how this function might be used:

<div class="code"><span codelanguage=""><table>
<tr>
<th></th>
</tr>
<tr>
<td>
<pre>uint32_t comparisonValue = XMVectorInBoundsR( V, Bounds );
if( XMComparisonAllInBounds( comparisonValue ) )
{
	DoStuff();
}</pre>
</td>
</tr>
</table></span></div>
The <code>DoStuff</code> function will be called only if all four components of <i>V</i> are within the volume
   determined by <i>Bounds</i> and -<i>Bounds</i>.

<h3><a id="Platform_Requirements"></a><a id="platform_requirements"></a><a id="PLATFORM_REQUIREMENTS"></a>Platform Requirements</h3>
Microsoft Visual Studio 2010 or Microsoft Visual Studio 2012 with the Windows SDK for Windows 8. Supported for Win32 desktop apps, Windows Store apps, and Windows Phone 8 apps.




## -see-also




<a href="https://msdn.microsoft.com/4d46fd96-55ca-cb66-f878-caf7894535ae">DirectXMath Library Utility Functions</a>



<a href="https://msdn.microsoft.com/a4ebab70-1fd6-455f-8078-aa85165d19ae">XMComparisonAllFalse</a>



<a href="https://msdn.microsoft.com/74d2856d-c311-47cd-9ff0-ee10ed66e29e">XMComparisonAllTrue</a>



<a href="https://msdn.microsoft.com/7ff34254-c7d4-4064-868e-2d7ed9351f2d">XMComparisonAnyFalse</a>



<a href="https://msdn.microsoft.com/fbd74d4a-2222-4e7f-bdb4-4650b3080bc4">XMComparisonAnyOutOfBounds</a>



<a href="https://msdn.microsoft.com/a268f858-00a7-4159-8940-9714cb479535">XMComparisonAnyTrue</a>



<a href="https://msdn.microsoft.com/72fafc98-a938-479c-9c1a-c2e37ceff9df">XMComparisonMixed</a>
 

 

