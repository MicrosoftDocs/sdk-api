---
UID: NF:msinkaut.IInkRecognitionAlternate.GetPropertyValue
title: IInkRecognitionAlternate::GetPropertyValue
author: windows-sdk-content
description: Retrieves the value of a specified property of the alternate.
old-location: tablet\iinkrecognitionalternate_getpropertyvalue.htm
old-project: tablet
ms.assetid: b2ebf45a-b995-4fbc-b86d-b94d1f48f659
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: ConfidenceLevel, GetPropertyValue, GetPropertyValue method [Tablet PC], GetPropertyValue method [Tablet PC],IInkRecognitionAlternate interface, HotPoint, IInkRecognitionAlternate interface [Tablet PC],GetPropertyValue method, IInkRecognitionAlternate.GetPropertyValue, IInkRecognitionAlternate::GetPropertyValue, LineMetrics, LineNumber, MaximumStrokeCount, PointsPerInch, S_OK, Segmentation, b2ebf45a-b995-4fbc-b86d-b94d1f48f659, msinkaut/IInkRecognitionAlternate::GetPropertyValue, tablet.iinkrecognitionalternate_getpropertyvalue
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: TabletPropertyMetricUnit
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	InkObj.dll
-	InkObj.dll.dll
api_name:
-	IInkRecognitionAlternate.GetPropertyValue
product: Windows
targetos: Windows
req.lib: InkObj.dll
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IInkRecognitionAlternate::GetPropertyValue


## -description



Retrieves the value of a specified property of the alternate.




## -parameters




### -param PropertyType [in]

Specifies which property of the alternate to return, as one of the GUIDs from the <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty</a> object.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


### -param PropertyValue [out, retval]

Upon return, contains the value of the property type as an array of bytes. this value is interpreted differently for each property type.

<table>
<tr>
<th>
                RecognitionProperty Type
              </th>
<th>
                Description
              </th>
</tr>
<tr>
<td width="40%"><a id="_________________ConfidenceLevel_______________"></a><a id="_________________confidencelevel_______________"></a><a id="_________________CONFIDENCELEVEL_______________"></a><dl>
<dt><b>
                ConfidenceLevel
              </b></dt>
</dl>
</td>
<td width="60%">

                CONFIDENCE_LEVEL enumeration type.
              

</td>
</tr>
<tr>
<td width="40%"><a id="_________________HotPoint_______________"></a><a id="_________________hotpoint_______________"></a><a id="_________________HOTPOINT_______________"></a><dl>
<dt><b>
                HotPoint
              </b></dt>
</dl>
</td>
<td width="60%">

                POINT.
              

</td>
</tr>
<tr>
<td width="40%"><a id="_________________LineMetrics_______________"></a><a id="_________________linemetrics_______________"></a><a id="_________________LINEMETRICS_______________"></a><dl>
<dt><b>
                LineMetrics
              </b></dt>
</dl>
</td>
<td width="60%">

                LATTICE_METRICS structure.
              

</td>
</tr>
<tr>
<td width="40%"><a id="_________________LineNumber_______________"></a><a id="_________________linenumber_______________"></a><a id="_________________LINENUMBER_______________"></a><dl>
<dt><b>
                LineNumber
              </b></dt>
</dl>
</td>
<td width="60%">

                ULONG.
              

</td>
</tr>
<tr>
<td width="40%"><a id="_________________MaximumStrokeCount_______________"></a><a id="_________________maximumstrokecount_______________"></a><a id="_________________MAXIMUMSTROKECOUNT_______________"></a><dl>
<dt><b>
                MaximumStrokeCount
              </b></dt>
</dl>
</td>
<td width="60%">

                Not used.
              

</td>
</tr>
<tr>
<td width="40%"><a id="_________________PointsPerInch_______________"></a><a id="_________________pointsperinch_______________"></a><a id="_________________POINTSPERINCH_______________"></a><dl>
<dt><b>
                PointsPerInch
              </b></dt>
</dl>
</td>
<td width="60%">

                Not used.
              

</td>
</tr>
<tr>
<td width="40%"><a id="_________________Segmentation_______________"></a><a id="_________________segmentation_______________"></a><a id="_________________SEGMENTATION_______________"></a><dl>
<dt><b>
                Segmentation
              </b></dt>
</dl>
</td>
<td width="60%">

                Not a value, returns TPC_E_INVALID_PROPERTY.
              

</td>
</tr>
<tr>
<td width="40%"><a id="_________________S_OK_______________"></a><a id="_________________s_ok_______________"></a><dl>
<dt><b>
                S_OK
              </b></dt>
</dl>
</td>
<td width="60%">

                Success.
              

</td>
</tr>
</table>
 


              For more information about the VARIANT structure, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.
            


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



 Use this method to obtain property values for <a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty</a> objects that have no corresponding helper property, such as the <a href="https://msdn.microsoft.com/049a5742-fc4f-4a9a-91d5-5eec56dc8e8b">Confidence</a> and <a href="https://msdn.microsoft.com/dd5578e7-7361-4e42-a503-2914f90a801f">LineNumber</a> properties.




## -see-also




<a href="https://msdn.microsoft.com/6c199960-e0ee-4370-a302-a45a3dbe8b28">AlternatesWithConstantPropertyValues Method</a>



<a href="https://msdn.microsoft.com/219e96ee-6492-4f76-9928-f2e8dc28493d">IInkRecognition Alternate Interface</a>



<a href="https://msdn.microsoft.com/2bfb0cbf-73a3-4e83-a4e9-f0803bd3dee8">RecognitionProperty Constants</a>
 

 

