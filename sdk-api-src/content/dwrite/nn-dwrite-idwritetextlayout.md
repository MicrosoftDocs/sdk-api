---
UID: NN:dwrite.IDWriteTextLayout
title: IDWriteTextLayout (dwrite.h)
author: windows-sdk-content
description: The IDWriteTextLayout interface represents a block of text after it has been fully analyzed and formatted.
old-location: directwrite\IDWriteTextLayout.htm
tech.root: DirectWrite
ms.assetid: 0d687337-8623-4014-967c-f533072e31cc
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IDWriteTextLayout, IDWriteTextLayout interface [Direct Write], IDWriteTextLayout interface [Direct Write],described, directwrite.IDWriteTextLayout, dwrite/IDWriteTextLayout
ms.topic: interface
f1_keywords: 
 - "dwrite/IDWriteTextLayout"
req.header: dwrite.h
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
req.lib: Dwrite.lib
req.dll: Dwrite.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dwrite.dll
api_name:
 - IDWriteTextLayout
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDWriteTextLayout interface


## -description


The <b>IDWriteTextLayout</b> interface represents a block of text after it has been fully analyzed and formatted.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextLayout</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>. <b>IDWriteTextLayout</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IDWriteTextLayout</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout-determineminwidth">DetermineMinWidth</a>
</td>
<td align="left" width="63%">
Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-draw">Draw</a>
</td>
<td align="left" width="63%">
 Draws text using the specified client drawing context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getclustermetrics">GetClusterMetrics</a>
</td>
<td align="left" width="63%">
 Retrieves logical properties and measurements of each glyph cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getdrawingeffect">GetDrawingEffect</a>
</td>
<td align="left" width="63%">
 Gets the application-defined drawing effect at the specified text position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getfontcollection">GetFontCollection</a>
</td>
<td align="left" width="63%">
 Gets the font collection associated with the text at the specified position.
    

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getfontfamilyname">GetFontFamilyName</a>
</td>
<td align="left" width="63%">
 Copies the font family name of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getfontfamilynamelength">GetFontFamilyNameLength</a>
</td>
<td align="left" width="63%">
 Get the length of the font family name at the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getfontsize">GetFontSize</a>
</td>
<td align="left" width="63%">
 Gets the font em height of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getfontstretch">GetFontStretch</a>
</td>
<td align="left" width="63%">
 Gets the font stretch of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getfontstyle">GetFontStyle</a>
</td>
<td align="left" width="63%">
 Gets the font style (also known as slope) of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getfontweight">GetFontWeight</a>
</td>
<td align="left" width="63%">
Gets the font weight of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getinlineobject">GetInlineObject</a>
</td>
<td align="left" width="63%">
 Gets the inline object at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getlinemetrics">GetLineMetrics</a>
</td>
<td align="left" width="63%">
Retrieves the information about each individual text line of the  text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getlocalename">GetLocaleName</a>
</td>
<td align="left" width="63%">
 Gets the locale name of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getlocalenamelength">GetLocaleNameLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the locale name of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getmaxheight">GetMaxHeight</a>
</td>
<td align="left" width="63%">
 Gets the layout maximum height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getmaxwidth">GetMaxWidth</a>
</td>
<td align="left" width="63%">
 Gets the layout maximum width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getmetrics">GetMetrics</a>
</td>
<td align="left" width="63%">
 Retrieves overall metrics for the formatted string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/DirectWrite/idwritetextlayout-getoverhangmetrics">GetOverhangMetrics</a>
</td>
<td align="left" width="63%">
Returns the overhangs (in DIPs) of the layout and all
    objects contained in it, including text glyphs and inline objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getstrikethrough">GetStrikethrough</a>
</td>
<td align="left" width="63%">
 Get the strikethrough presence of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-gettypography">GetTypography</a>
</td>
<td align="left" width="63%">
 Gets the typography setting of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-getunderline">GetUnderline</a>
</td>
<td align="left" width="63%">
 Gets the underline presence of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-hittestpoint">HitTestPoint</a>
</td>
<td align="left" width="63%">
 The application calls this function passing in a specific pixel location
     relative to the top-left location of the layout box and obtains the
     information about the correspondent hit-test metrics of the text string
     where the hit-test has occurred. When the specified pixel location is
     outside the text string, the function sets the output value <i>*isInside</i> to
     <b>FALSE</b>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-hittesttextposition">HitTestTextPosition</a>
</td>
<td align="left" width="63%">
 The application calls this function to get the pixel location relative
     to the top-left of the layout box given the text position and the
     logical side of the position. This function is normally used as part of
     caret positioning of text where the caret is drawn at the location
     corresponding to the current text editing position. It may also be used
     as a way to programmatically obtain the geometry of a particular text
     position in UI automation.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-hittesttextrange">HitTestTextRange</a>
</td>
<td align="left" width="63%">
 The application calls this function to get a set of hit-test metrics corresponding to a range of text positions. One of the main usages is to implement highlight selection of the text string. 

The function returns E_NOT_SUFFICIENT_BUFFER, which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER), when the buffer size of hitTestMetrics is too small to hold all the regions calculated by the function. In this situation, the function sets the output value *actualHitTestMetricsCount to the number of geometries calculated. 

The application is responsible for allocating a new buffer of greater size and calling the function again.

A good value to use as an initial value for maxHitTestMetricsCount may be calculated from the following equation:


<pre class="syntax" xml:space="preserve"><code>maxHitTestMetricsCount = lineCount * maxBidiReorderingDepth</code></pre>


where lineCount is obtained from the value of the output argument
     *actualLineCount (from the function <b>IDWriteTextLayout</b>::GetLineLengths),
     and the maxBidiReorderingDepth value from the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_text_metrics">DWRITE_TEXT_METRICS</a>structure of the output argument *textMetrics (from the function
     <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritefactory">IDWriteFactory</a>::<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">CreateTextLayout</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setdrawingeffect">SetDrawingEffect</a>
</td>
<td align="left" width="63%">
 Sets the application-defined drawing effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setfontcollection">SetFontCollection</a>
</td>
<td align="left" width="63%">
 Sets the font collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setfontfamilyname">SetFontFamilyName</a>
</td>
<td align="left" width="63%">
 Sets null-terminated font family name for text within a specified  text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setfontsize">SetFontSize</a>
</td>
<td align="left" width="63%">
Sets the font size in DIP units for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setfontstretch">SetFontStretch</a>
</td>
<td align="left" width="63%">
 Sets the  font stretch for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setfontstyle">SetFontStyle</a>
</td>
<td align="left" width="63%">
 Sets the font style for  text within a text range specified by a <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setfontweight">SetFontWeight</a>
</td>
<td align="left" width="63%">
 Sets the font weight for text within a text range specified by a <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setinlineobject">SetInlineObject</a>
</td>
<td align="left" width="63%">
 Sets the inline object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setlocalename">SetLocaleName</a>
</td>
<td align="left" width="63%">
 Sets the locale name for text
    within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setmaxheight">SetMaxHeight</a>
</td>
<td align="left" width="63%">
 Sets the layout maximum height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setmaxwidth">SetMaxWidth</a>
</td>
<td align="left" width="63%">
 Sets the layout maximum width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setstrikethrough">SetStrikethrough</a>
</td>
<td align="left" width="63%">
Sets strikethrough for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-settypography">SetTypography</a>
</td>
<td align="left" width="63%">
 Sets  font typography features for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-setunderline">SetUnderline</a>
</td>
<td align="left" width="63%">
Sets underlining for text within a specified text range.

</td>
</tr>
</table> 


## -remarks



To get a reference to the <b>IDWriteTextLayout</b> interface, the application must call the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritefactory-createtextlayout">IDWriteFactory::CreateTextLayout</a> method, as shown in the following code.  


```cpp

// Create a text layout using the text format.
if (SUCCEEDED(hr))
{
    RECT rect;
    GetClientRect(hwnd_, &rect); 
    float width  = rect.right  / dpiScaleX_;
    float height = rect.bottom / dpiScaleY_;

    hr = pDWriteFactory_->CreateTextLayout(
        wszText_,      // The string to be laid out and formatted.
        cTextLength_,  // The length of the string.
        pTextFormat_,  // The text format to apply to the string (contains font information, etc).
        width,         // The width of the layout box.
        height,        // The height of the layout box.
        &pTextLayout_  // The IDWriteTextLayout interface pointer.
        );
}


```


The <b>IDWriteTextLayout</b> interface allows the application to change the format for ranges of the text it represents, specified by a <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/ns-dwrite-dwrite_text_range">DWRITE_TEXT_RANGE</a> structure.   The following example shows how to set the font weight for a text range.


```cpp

// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 4};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}


```


<b>IDWriteTextLayout</b> also provides methods for adding strikethrough,  underline, and inline objects to the text.

To draw the block of text represented by an <b>IDWriteTextLayout</b> object, <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> provides the <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">ID2D1RenderTarget::DrawTextLayout</a> method. To draw using a custom renderer implement an <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a> interface and  call the  <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a> method

<h3><a id="DirectWrite_and_Direct2D"></a><a id="directwrite_and_direct2d"></a><a id="DIRECTWRITE_AND_DIRECT2D"></a>DirectWrite and Direct2D</h3>
To draw a formatted string represented by an <b>IDWriteTextLayout</b> object, <a href="https://docs.microsoft.com/windows/desktop/Direct2D/direct2d-portal">Direct2D</a> provides the  <a href="https://docs.microsoft.com/windows/desktop/api/d2d1/nf-d2d1-id2d1rendertarget-drawtextlayout">ID2D1RenderTarget::DrawTextLayout</a> method.

<h3><a id="Other_Rendering_Options"></a><a id="other_rendering_options"></a><a id="OTHER_RENDERING_OPTIONS"></a>Other Rendering Options</h3>
To render using a custom renderer, use the <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nf-dwrite-idwritetextlayout-draw">IDWriteTextLayout::Draw</a> method, which takes a callback interface derived from <a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a> as an argument, as shown in the following code.


```cpp

// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );


```



<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextrenderer">IDWriteTextRenderer</a> declares methods for drawing a glyph run, underline, strikethrough and inline objects.  It is up to the application to implement these methods.  Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.

Using a custom text renderer also enables you to render using another technology, such as GDI.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/dwrite/nn-dwrite-idwritetextformat">IDWriteTextFormat</a>
 

 

