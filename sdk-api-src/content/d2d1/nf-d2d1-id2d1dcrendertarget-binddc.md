---
UID: NF:d2d1.ID2D1DCRenderTarget.BindDC
title: ID2D1DCRenderTarget::BindDC
author: windows-sdk-content
description: Binds the render target to the device context to which it issues drawing commands.
old-location: direct2d\ID2D1DCRenderTarget_BindDC.htm
tech.root: direct2d
ms.assetid: a5e98470-9a9f-4a85-b00f-afb2ead3fb31
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: BindDC, BindDC method [Direct2D], BindDC method [Direct2D],ID2D1DCRenderTarget interface, ID2D1DCRenderTarget interface [Direct2D],BindDC method, ID2D1DCRenderTarget.BindDC, ID2D1DCRenderTarget::BindDC, d2d1/ID2D1DCRenderTarget::BindDC, direct2d.ID2D1DCRenderTarget_BindDC
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: d2d1.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: D2d1.lib
req.dll: D2d1.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - D2d1.dll
api_name:
 - ID2D1DCRenderTarget.BindDC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ID2D1DCRenderTarget::BindDC


## -description


Binds the render target to the device context to which it issues drawing commands.


## -parameters




### -param hDC

Type: <b>const HDC</b>

The device context to which the render target issues drawing commands.


### -param pSubRect [in]

Type: <b>const <a href="https://msdn.microsoft.com/9439cb6c-f2f7-4c27-b1d7-8ddf16d81fe8">RECT</a>*</b>

The dimensions of the handle to a device context (HDC) to which the render target is bound. 


## -returns



Type: <b><a href="455d07e9-52c3-4efb-a9dc-2955cbfd38cc">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Before you can render with the DC render target, you must use its <b>BindDC</b> method to associate it with a GDI DC.  You do this each time you  use a different DC, or the size of the area you want to draw to changes.


#### Examples

In the preceding code, <i>m_pD2DFactory</i> is a  pointer to an <a href="https://msdn.microsoft.com/cef6115c-98e8-49e6-b419-271b43ce2938">ID2D1Factory</a>, and <i>m_pDCRT</i> is a pointer to an <a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a>. 

The next code example binds a DC to the <a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>HRESULT DemoApp::OnRender(const PAINTSTRUCT &amp;ps)
{
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Get the dimensions of the client drawing area.
GetClientRect(m_hwnd, &amp;rc);
</pre>
</td>
</tr>
</table></span><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>// Bind the DC to the DC render target.
hr = m_pDCRT-&gt;BindDC(ps.hdc, &amp;rc);
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/182df2dc-2574-4d8f-a7e1-30d70da1740a">Direct2D and GDI Interoperation Overview</a>



<a href="https://msdn.microsoft.com/6546998e-6740-413a-88c5-36fa0decec8f">ID2D1DCRenderTarget</a>
 

 

