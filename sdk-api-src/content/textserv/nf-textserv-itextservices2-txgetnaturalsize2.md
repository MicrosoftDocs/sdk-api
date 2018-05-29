---
UID: NF:textserv.ITextServices2.TxGetNaturalSize2
title: ITextServices2::TxGetNaturalSize2
author: windows-sdk-content
description: Resizes a control so it fits its content appropriately. This method is similar to TxGetNaturalSize, but also retrieves the ascent of the top line of text.
old-location: controls\itextservices2_txgetnaturalsize2.htm
old-project: Controls
ms.assetid: 9D9A3D06-5C1F-4D50-B7B7-E6CA2BFDB89C
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: ITextServices2 interface [Windows Controls],TxGetNaturalSize2 method, ITextServices2.TxGetNaturalSize2, ITextServices2::TxGetNaturalSize2, TXTNS_EMU, TXTNS_FITTOCONTENT, TXTNS_FITTOCONTENT2, TXTNS_FITTOCONTENT3, TXTNS_FITTOCONTENTWSP, TXTNS_INCLUDELASTLINE, TXTNS_ROUNDTOLINE, TxGetNaturalSize2, TxGetNaturalSize2 method [Windows Controls], TxGetNaturalSize2 method [Windows Controls],ITextServices2 interface, controls.itextservices2_txgetnaturalsize2, textserv/ITextServices2::TxGetNaturalSize2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: textserv.h
req.include-header: 
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
req.typenames: TMGR_DIRECTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msftedit.dll
api_name:
-	ITextServices2.TxGetNaturalSize2
product: Windows
targetos: Windows
req.lib: 
req.dll: Msftedit.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITextServices2::TxGetNaturalSize2


## -description


Resizes a control so it fits its content appropriately. This method is similar to <a href="https://msdn.microsoft.com/66798915-af6f-4a18-813b-872bf0298824">TxGetNaturalSize</a>, but also retrieves the ascent of the top line of text.


## -parameters




### -param dwAspect

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The aspect for the drawing. It can be any of the values from the <a href="https://msdn.microsoft.com/a2b729c8-7091-4520-93cd-c44468ba0274">DVASPECT</a> enumeration. 


### -param hdcDraw

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

The device context into which drawing occurs. 


### -param hicTargetDev

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HDC</a></b>

The device context for which text should be formatted (that is, for WYSIWYG). 


### -param ptd

Type: <b><a href="https://msdn.microsoft.com/724ff714-c170-4d06-92cb-e042e41c0af2">DVTARGETDEVICE</a>*</b>

More information on the target device.


### -param dwMode

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The type of fitting requested. It can be one of the following.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TXTNS_EMU"></a><a id="txtns_emu"></a><dl>
<dt><b>TXTNS_EMU</b></dt>
</dl>
</td>
<td width="60%">
 Use English Metric Units (EMUs) instead of pixels as  										the measuring units (both ways) for this method's parameters.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTNS_FITTOCONTENT"></a><a id="txtns_fittocontent"></a><dl>
<dt><b>TXTNS_FITTOCONTENT</b></dt>
</dl>
</td>
<td width="60%">
Resize the control to fit the entire text by formatting the text to the width that is passed in. The text services object returns the height of the entire text and the width of the widest line.

For example, this should be done when the user double-clicks one of the control's handles.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTNS_FITTOCONTENT2"></a><a id="txtns_fittocontent2"></a><dl>
<dt><b>TXTNS_FITTOCONTENT2</b></dt>
</dl>
</td>
<td width="60%">

                
              Resize the control so that it fits indented content.  

</td>
</tr>
<tr>
<td width="40%"><a id="TXTNS_FITTOCONTENT3"></a><a id="txtns_fittocontent3"></a><dl>
<dt><b>TXTNS_FITTOCONTENT3</b></dt>
</dl>
</td>
<td width="60%">

                
                
              Resize the control so that it fits indented  										content and trailing white space.  

</td>
</tr>
<tr>
<td width="40%"><a id="TXTNS_FITTOCONTENTWSP"></a><a id="txtns_fittocontentwsp"></a><dl>
<dt><b>TXTNS_FITTOCONTENTWSP</b></dt>
</dl>
</td>
<td width="60%">

                
                
              Resize the control so that it fits unindented  										content and trailing white space.  

</td>
</tr>
<tr>
<td width="40%"><a id="TXTNS_INCLUDELASTLINE"></a><a id="txtns_includelastline"></a><dl>
<dt><b>TXTNS_INCLUDELASTLINE</b></dt>
</dl>
</td>
<td width="60%">
 For a plain-text control, include the height of the final carriage return when calculating the size.

</td>
</tr>
<tr>
<td width="40%"><a id="TXTNS_ROUNDTOLINE"></a><a id="txtns_roundtoline"></a><dl>
<dt><b>TXTNS_ROUNDTOLINE</b></dt>
</dl>
</td>
<td width="60%">
Resize the control to show an integral number of lines (no line is clipped). Format enough text to fill the width and height that is passed in, and then return a height that is rounded to the nearest line boundary.


<div class="alert"><b>Note</b>  The passed and returned width and height correspond to the view rectangle. The host should adjust back to the client rectangle as needed. Because these values represent the extent of the text object, they are input and output in HIMETRIC coordinates (each HIMETRIC unit is 0.01 millimeter), and measuring does not include any zoom factor. For a discussion of the zoom factor, see <a href="https://msdn.microsoft.com/03cf4acc-f70e-40a4-9050-6e6777867b2b">TxGetExtent</a>.</div>
<div> </div>


</td>
</tr>
</table>
 


### -param psizelExtent

Type: <b>const SIZEL*</b>

Sizes of extents (in HIMETRIC units) to use for zooming. 


### -param pwidth

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The width for the fitting defined by <i>dwMode</i>. 


### -param pheight

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

The height for the fitting defined by <i>dwMode</i>. 


### -param pascent

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a>*</b>

For single-line controls, receives the ascent (units above the baseline) of characters in the top line of text. 


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the method succeeds, the return value is <b>S_OK</b>.

If text services could not activate the object, the return value is one of the following <b>HRESULT</b> codes. For more information on COM error codes, see <a href="https://msdn.microsoft.com/15f3ae3e-1794-4948-a7aa-6309a703364b">Error Handling in COM</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
Unable to determine correct size.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more arguments are not valid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory.

</td>
</tr>
</table>
 




## -remarks



The first four parameters are similar to equivalent parameters in <a href="https://msdn.microsoft.com/5fb14a41-2e73-4760-ba77-f1bfd2a1184b">ITextServices::TxDraw</a> and give the same information. In the case where the lines must be recalculated, <b>TxGetNaturalSize2</b>  uses these values in the same ways as in <b>ITextServices::TxDraw</b>.

The <i>pwidth</i> and <i>pheight</i> parameters are in/out parameters. The host passes in the tentative width and height of the natural extent of the text object. The text services object compares these values against its current cached state, and if different, recalculates lines. Then, it computes and returns the natural size, as specified by <i>dwMode</i>. 


#### Examples

The following example shows how to initialize the <i>psizelExtent</i> parameter for to a zoom factor of 1:1. The ellipses indicate code that you need to provide.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>
LONG dxpi = GetDeviceCaps(hdc, LOGPIXELSX);
LONG dypi = GetDeviceCaps(hdc, LOGPIXELSY);
LONG dyAscent = 0;
LONG dx = ... ;  // Text image width, in pixels 
LONG dy = ... ;  // Text image height, in pixels 
SIZEL sizel;     // dx and dy, in HIMETRIC

ITextServices2 *pserv = ... ; // Interface for single-line control

sizel.cx = MulDiv(dx, HIMETRIC_PER_INCH, dxpi); 
sizel.cy = MulDiv(dy, HIMETRIC_PER_INCH, dypi);

pserv-&gt;TxGetNaturalSize2(DVASPECT_DOCPRINT, hdc, hdcNil, pNil,
    TXTNS_FITTOCONTENT, &amp;sizel, &amp;dx, &amp;dy, &amp;dyAscent))) 
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/B5DC90BA-F9A5-45DC-8C8A-784380C38769">ITextServices2</a>
 

 

