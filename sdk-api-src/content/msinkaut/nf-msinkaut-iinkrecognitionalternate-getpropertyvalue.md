---
UID: NF:msinkaut.IInkRecognitionAlternate.GetPropertyValue
title: IInkRecognitionAlternate::GetPropertyValue (msinkaut.h)
description: Retrieves the value of a specified property of the alternate.
helpviewer_keywords: ["ConfidenceLevel","GetPropertyValue","GetPropertyValue method [Tablet PC]","GetPropertyValue method [Tablet PC]","IInkRecognitionAlternate interface","HotPoint","IInkRecognitionAlternate interface [Tablet PC]","GetPropertyValue method","IInkRecognitionAlternate.GetPropertyValue","IInkRecognitionAlternate::GetPropertyValue","LineMetrics","LineNumber","MaximumStrokeCount","PointsPerInch","S_OK","Segmentation","b2ebf45a-b995-4fbc-b86d-b94d1f48f659","msinkaut/IInkRecognitionAlternate::GetPropertyValue","tablet.iinkrecognitionalternate_getpropertyvalue"]
old-location: tablet\iinkrecognitionalternate_getpropertyvalue.htm
tech.root: tablet
ms.assetid: b2ebf45a-b995-4fbc-b86d-b94d1f48f659
ms.date: 12/05/2018
ms.keywords: ConfidenceLevel, GetPropertyValue, GetPropertyValue method [Tablet PC], GetPropertyValue method [Tablet PC],IInkRecognitionAlternate interface, HotPoint, IInkRecognitionAlternate interface [Tablet PC],GetPropertyValue method, IInkRecognitionAlternate.GetPropertyValue, IInkRecognitionAlternate::GetPropertyValue, LineMetrics, LineNumber, MaximumStrokeCount, PointsPerInch, S_OK, Segmentation, b2ebf45a-b995-4fbc-b86d-b94d1f48f659, msinkaut/IInkRecognitionAlternate::GetPropertyValue, tablet.iinkrecognitionalternate_getpropertyvalue
req.header: msinkaut.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP Tablet PC Edition [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: InkObj.dll
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IInkRecognitionAlternate::GetPropertyValue
 - msinkaut/IInkRecognitionAlternate::GetPropertyValue
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognitionAlternate.GetPropertyValue
---

# IInkRecognitionAlternate::GetPropertyValue


## -description

Retrieves the value of a specified property of the alternate.

## -parameters

### -param PropertyType [in]

Specifies which property of the alternate to return, as one of the GUIDs from the <a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a> object.

For more information about the BSTR data type, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

### -param PropertyValue [out, retval]

Upon return, contains the value of the property type as an array of bytes. this value is interpreted differently for each property type.

<table>
<tr>
<th>RecognitionProperty Type
              </th>
<th>Description
              </th>
</tr>
<tr>
<td width="40%"><a id="ConfidenceLevel_______________"></a><a id="confidencelevel_______________"></a><a id="CONFIDENCELEVEL_______________"></a><dl>
<dt><b>ConfidenceLevel
              </b></dt>
</dl>
</td>
<td width="60%">
CONFIDENCE_LEVEL enumeration type.
              

</td>
</tr>
<tr>
<td width="40%"><a id="HotPoint_______________"></a><a id="hotpoint_______________"></a><a id="HOTPOINT_______________"></a><dl>
<dt><b>HotPoint
              </b></dt>
</dl>
</td>
<td width="60%">
POINT.
              

</td>
</tr>
<tr>
<td width="40%"><a id="LineMetrics_______________"></a><a id="linemetrics_______________"></a><a id="LINEMETRICS_______________"></a><dl>
<dt><b>LineMetrics
              </b></dt>
</dl>
</td>
<td width="60%">
LATTICE_METRICS structure.
              

</td>
</tr>
<tr>
<td width="40%"><a id="LineNumber_______________"></a><a id="linenumber_______________"></a><a id="LINENUMBER_______________"></a><dl>
<dt><b>LineNumber
              </b></dt>
</dl>
</td>
<td width="60%">
ULONG.
              

</td>
</tr>
<tr>
<td width="40%"><a id="MaximumStrokeCount_______________"></a><a id="maximumstrokecount_______________"></a><a id="MAXIMUMSTROKECOUNT_______________"></a><dl>
<dt><b>MaximumStrokeCount
              </b></dt>
</dl>
</td>
<td width="60%">
Not used.
              

</td>
</tr>
<tr>
<td width="40%"><a id="PointsPerInch_______________"></a><a id="pointsperinch_______________"></a><a id="POINTSPERINCH_______________"></a><dl>
<dt><b>PointsPerInch
              </b></dt>
</dl>
</td>
<td width="60%">
Not used.
              

</td>
</tr>
<tr>
<td width="40%"><a id="Segmentation_______________"></a><a id="segmentation_______________"></a><a id="SEGMENTATION_______________"></a><dl>
<dt><b>Segmentation
              </b></dt>
</dl>
</td>
<td width="60%">
Not a value, returns TPC_E_INVALID_PROPERTY.
              

</td>
</tr>
<tr>
<td width="40%"><a id="S_OK_______________"></a><a id="s_ok_______________"></a><dl>
<dt><b>S_OK
              </b></dt>
</dl>
</td>
<td width="60%">
Success.
              

</td>
</tr>
</table>
 

For more information about the VARIANT structure, see <a href="/windows/desktop/tablet/using-the-com-library">Using the COM Library</a>.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INK_EXCEPTION</b></dt>
</dl>
</td>
<td width="60%">
An exception occurred while processing.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
A parameter contained an invalid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>CO_E_CLASSSTRING</b></dt>
</dl>
</td>
<td width="60%">
Invalid GUID format.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The flag is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory to complete the operation.

</td>
</tr>
</table>

## -remarks

 Use this method to obtain property values for <a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty</a> objects that have no corresponding helper property, such as the <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_confidence">Confidence</a> and <a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-get_linenumber">LineNumber</a> properties.

## -see-also

<a href="/windows/desktop/api/msinkaut/nf-msinkaut-iinkrecognitionalternate-alternateswithconstantpropertyvalues">AlternatesWithConstantPropertyValues Method</a>



<a href="/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognitionalternate">IInkRecognition Alternate Interface</a>



<a href="/windows/desktop/tablet/recognitionproperty-constants">RecognitionProperty Constants</a>