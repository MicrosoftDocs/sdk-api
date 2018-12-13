---
UID: NN:dwrite.IDWriteTextLayout
title: IDWriteTextLayout
author: windows-sdk-content
description: The IDWriteTextLayout interface represents a block of text after it has been fully analyzed and formatted.
old-location: directwrite\IDWriteTextLayout.htm
tech.root: DirectWrite
ms.assetid: 0d687337-8623-4014-967c-f533072e31cc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDWriteTextLayout, IDWriteTextLayout interface [Direct Write], IDWriteTextLayout interface [Direct Write],described, directwrite.IDWriteTextLayout, dwrite/IDWriteTextLayout
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
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
---

# IDWriteTextLayout interface


## -description


The <b>IDWriteTextLayout</b> interface represents a block of text after it has been fully analyzed and formatted.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IDWriteTextLayout</b> interface inherits from <a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>. <b>IDWriteTextLayout</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/8efa1471-1b74-46d4-ac6d-fb1839ce2e74">DetermineMinWidth</a>
</td>
<td align="left" width="63%">
Determines the minimum possible width the layout can be set to without emergency breaking between the characters of whole words occurring.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">Draw</a>
</td>
<td align="left" width="63%">
 Draws text using the specified client drawing context.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3c8ca925-2149-48dc-a71a-4f6a40153c3e">GetClusterMetrics</a>
</td>
<td align="left" width="63%">
 Retrieves logical properties and measurements of each glyph cluster.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1b8d30d1-4da0-40bc-9fee-d06eccae6539">GetDrawingEffect</a>
</td>
<td align="left" width="63%">
 Gets the application-defined drawing effect at the specified text position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce3e4510-2b40-4eb4-aaf8-fe830e96d618">GetFontCollection</a>
</td>
<td align="left" width="63%">
 Gets the font collection associated with the text at the specified position.
    

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5283d1f-8a40-4272-b71c-590b6bc6a340">GetFontFamilyName</a>
</td>
<td align="left" width="63%">
 Copies the font family name of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e3b3d111-04a7-409b-98dd-b0fc3947f24b">GetFontFamilyNameLength</a>
</td>
<td align="left" width="63%">
 Get the length of the font family name at the current position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/31cf375a-d749-4af1-9470-73439fe6276e">GetFontSize</a>
</td>
<td align="left" width="63%">
 Gets the font em height of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f72cdbbf-71ca-45fe-8250-c920c82519e3">GetFontStretch</a>
</td>
<td align="left" width="63%">
 Gets the font stretch of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/184aa6c8-4dc5-4881-a0e0-61dc0b1a8240">GetFontStyle</a>
</td>
<td align="left" width="63%">
 Gets the font style (also known as slope) of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1c86c8e-f6d2-4c72-9117-f8ae4334a71b">GetFontWeight</a>
</td>
<td align="left" width="63%">
Gets the font weight of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0d86f2a4-d046-4d27-b128-40f2a3dd359a">GetInlineObject</a>
</td>
<td align="left" width="63%">
 Gets the inline object at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/30f49632-d7fa-44e2-b289-2ad658e0c867">GetLineMetrics</a>
</td>
<td align="left" width="63%">
Retrieves the information about each individual text line of the  text string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6d0c0609-f568-41cd-9d3f-37ff92174e29">GetLocaleName</a>
</td>
<td align="left" width="63%">
 Gets the locale name of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/65d05939-ed51-45e9-a556-71a8cf52b196">GetLocaleNameLength</a>
</td>
<td align="left" width="63%">
 Gets the length of the locale name of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/841b48aa-690a-4563-a303-2990f4233d07">GetMaxHeight</a>
</td>
<td align="left" width="63%">
 Gets the layout maximum height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/05706f92-6bf6-49fe-9b63-bf8350d48bd9">GetMaxWidth</a>
</td>
<td align="left" width="63%">
 Gets the layout maximum width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cbfafccc-f66c-4b75-9540-e393ee203859">GetMetrics</a>
</td>
<td align="left" width="63%">
 Retrieves overall metrics for the formatted string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4b23f6c5-cacc-41e2-8934-6f95208b999a">GetOverhangMetrics</a>
</td>
<td align="left" width="63%">
Returns the overhangs (in DIPs) of the layout and all
    objects contained in it, including text glyphs and inline objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/39a1af39-a8b3-47b2-b3cb-8e807ae202c9">GetStrikethrough</a>
</td>
<td align="left" width="63%">
 Get the strikethrough presence of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cb7d8bf5-8368-426d-a321-f5c9ef8c7d40">GetTypography</a>
</td>
<td align="left" width="63%">
 Gets the typography setting of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cd34ba6b-748c-44ca-8db6-d4715a057def">GetUnderline</a>
</td>
<td align="left" width="63%">
 Gets the underline presence of the text at the specified position.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6eb10e03-beb6-4ad3-9b57-4b4be0e265de">HitTestPoint</a>
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
<a href="https://msdn.microsoft.com/a7a8d82a-74a6-4e4a-a57d-60194e20a087">HitTestTextPosition</a>
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
<a href="https://msdn.microsoft.com/970ea72c-d097-42c2-9d93-774387ba7881">HitTestTextRange</a>
</td>
<td align="left" width="63%">
 The application calls this function to get a set of hit-test metrics
     corresponding to a range of text positions. One of the main usages
     is to implement highlight selection of the text string. The
     function returns E_NOT_SUFFICIENT_BUFFER, which is equivalent to HRESULT_FROM_WIN32(ERROR_INSUFFICIENT_BUFFER), when the buffer size of
     hitTestMetrics is too small to hold all the regions calculated by the
     function. In this situation, the function sets the output value
     *actualHitTestMetricsCount to the number of geometries calculated.
     The application is responsible for allocating a new buffer of greater
     size and calling the function again.
    
     A good value to use as an initial value for maxHitTestMetricsCount may
     be calculated from the following equation:
         maxHitTestMetricsCount = lineCount * maxBidiReorderingDepth
    
     where lineCount is obtained from the value of the output argument
     *actualLineCount (from the function <b>IDWriteTextLayout</b>::GetLineLengths),
     and the maxBidiReorderingDepth value from the <a href="https://msdn.microsoft.com/4524ace3-fca6-4daf-9ecb-516771e53fc9">DWRITE_TEXT_METRICS</a>structure of the output argument *textMetrics (from the function
     <a href="https://msdn.microsoft.com/73a85977-5c24-4abc-ad8c-1d0d6474bd7e">IDWriteFactory</a>::<a href="https://msdn.microsoft.com/f76f85df-112f-4bc3-b922-a0d7940d2954">CreateTextLayout</a>).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d3269f8e-c1bc-4e84-92cb-a8899a0268ff">SetDrawingEffect</a>
</td>
<td align="left" width="63%">
 Sets the application-defined drawing effect.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e80038bd-e157-4f76-85c7-559cadacb5c4">SetFontCollection</a>
</td>
<td align="left" width="63%">
 Sets the font collection.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c5da17d1-46af-4865-9a6e-a35c6907491b">SetFontFamilyName</a>
</td>
<td align="left" width="63%">
 Sets null-terminated font family name for text within a specified  text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/73698726-e329-4367-87be-f2043e1f5591">SetFontSize</a>
</td>
<td align="left" width="63%">
Sets the font size in DIP units for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/34e7e476-abed-4b0f-a18d-662a277548b1">SetFontStretch</a>
</td>
<td align="left" width="63%">
 Sets the  font stretch for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/688a6c30-5eca-44aa-bcb0-02a3f29647b8">SetFontStyle</a>
</td>
<td align="left" width="63%">
 Sets the font style for  text within a text range specified by a <a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c6b65548-c486-4006-afe9-95bc628bbf70">SetFontWeight</a>
</td>
<td align="left" width="63%">
 Sets the font weight for text within a text range specified by a <a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a> structure.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/19fc9dd8-d732-4078-9db3-bad18681c7ea">SetInlineObject</a>
</td>
<td align="left" width="63%">
 Sets the inline object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c00d28dc-5338-438f-9046-5ad54e845e9d">SetLocaleName</a>
</td>
<td align="left" width="63%">
 Sets the locale name for text
    within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5d71a597-7b7d-402f-a2e6-b41f5cadf061">SetMaxHeight</a>
</td>
<td align="left" width="63%">
 Sets the layout maximum height.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/49889f71-4650-4f16-a130-d0437bd50b52">SetMaxWidth</a>
</td>
<td align="left" width="63%">
 Sets the layout maximum width.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/650063e7-186e-493f-8e06-5466cc69e3f3">SetStrikethrough</a>
</td>
<td align="left" width="63%">
Sets strikethrough for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ee0702fb-a3ff-442b-bd3b-6ff35fcba0ec">SetTypography</a>
</td>
<td align="left" width="63%">
 Sets  font typography features for text within a specified text range.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/677bb4e2-4ae9-4e79-96a3-d4961e317886">SetUnderline</a>
</td>
<td align="left" width="63%">
Sets underlining for text within a specified text range.

</td>
</tr>
</table> 


## -remarks



To get a reference to the <b>IDWriteTextLayout</b> interface, the application must call the <a href="https://msdn.microsoft.com/f76f85df-112f-4bc3-b922-a0d7940d2954">IDWriteFactory::CreateTextLayout</a> method, as shown in the following code.  


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


The <b>IDWriteTextLayout</b> interface allows the application to change the format for ranges of the text it represents, specified by a <a href="https://msdn.microsoft.com/2e37e060-69b9-4ca2-9d95-8e9a39f6cf83">DWRITE_TEXT_RANGE</a> structure.   The following example shows how to set the font weight for a text range.


```cpp

// Set the font weight to bold for the first 5 letters.
DWRITE_TEXT_RANGE textRange = {0, 4};

if (SUCCEEDED(hr))
{
    hr = pTextLayout_->SetFontWeight(DWRITE_FONT_WEIGHT_BOLD, textRange);
}


```


<b>IDWriteTextLayout</b> also provides methods for adding strikethrough,  underline, and inline objects to the text.

To draw the block of text represented by an <b>IDWriteTextLayout</b> object, <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> provides the <a href="https://msdn.microsoft.com/9356071a-35ca-462a-8a77-887e63850586">ID2D1RenderTarget::DrawTextLayout</a> method. To draw using a custom renderer implement an <a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a> interface and  call the  <a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">IDWriteTextLayout::Draw</a> method

<h3><a id="DirectWrite_and_Direct2D"></a><a id="directwrite_and_direct2d"></a><a id="DIRECTWRITE_AND_DIRECT2D"></a>DirectWrite and Direct2D</h3>
To draw a formatted string represented by an <b>IDWriteTextLayout</b> object, <a href="https://msdn.microsoft.com/03b3b91c-9751-4f8d-af24-85067f06930b">Direct2D</a> provides the  <a href="https://msdn.microsoft.com/9356071a-35ca-462a-8a77-887e63850586">ID2D1RenderTarget::DrawTextLayout</a> method.

<h3><a id="Other_Rendering_Options"></a><a id="other_rendering_options"></a><a id="OTHER_RENDERING_OPTIONS"></a>Other Rendering Options</h3>
To render using a custom renderer, use the <a href="https://msdn.microsoft.com/8d92a7c3-4804-47f6-bfca-5322be119cbb">IDWriteTextLayout::Draw</a> method, which takes a callback interface derived from <a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a> as an argument, as shown in the following code.


```cpp

// Draw the text layout using DirectWrite and the CustomTextRenderer class.
hr = pTextLayout_->Draw(
        NULL,
        pTextRenderer_,  // Custom text renderer.
        origin.x,
        origin.y
        );


```



<a href="https://msdn.microsoft.com/a2ac70c8-e33b-46f1-b53b-1ab07555f109">IDWriteTextRenderer</a> declares methods for drawing a glyph run, underline, strikethrough and inline objects.  It is up to the application to implement these methods.  Creating a custom text renderer allows the application to apply additional effects when rendering text, such as a custom fill or outline.

Using a custom text renderer also enables you to render using another technology, such as GDI.




## -see-also




<a href="https://msdn.microsoft.com/64b2cac3-c4cb-4213-b808-7b279d296939">IDWriteTextFormat</a>
 

 

