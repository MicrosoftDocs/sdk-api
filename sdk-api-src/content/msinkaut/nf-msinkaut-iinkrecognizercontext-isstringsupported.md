---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IInkRecognizerContext::IsStringSupported


## -description



Indicates whether the system dictionary, user dictionary, or <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">word list</a> contain a specified string.




## -parameters




### -param String




### -param Supported [out, retval]

When this method returns, contains <b>VARIANT_TRUE</b> if the string is in the dictionary or word list; otherwise <b>VARIANT_FALSE</b>.


#### - s [in]

The string to look up in the dictionaries and word list.

For more information about the BSTR data type, see <a href="https://msdn.microsoft.com/fa43fad9-804c-42d9-9717-6686d5f98ed8">Using the COM Library</a>.


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
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
One of the dictionaries contains the string.

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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid input string.

</td>
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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Cannot allocate memory operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Unexpected parameter or property type.

</td>
</tr>
</table>
 




## -remarks



This method considers all flags and factoid, among other things, that give context to the string that is being tested.

This method does not search the user dictionary if you specify a <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">word list</a> for the context. The recognizer uses the speech dictionary in Microsoft Office XP.

Use the <a href="https://msdn.microsoft.com/11a76706-e2e5-4ae5-bdc2-5354514ea29f">Factoid</a> property to limit the search to the system dictionary or the word list that is associated with the context. For example, to limit the search to the system dictionary, specify the <a href="https://msdn.microsoft.com/247a1f7d-8205-4e4d-9cfc-daad9bd2191f">SystemDictionary</a> factoid. To improve the results, you may also need to set the <a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags</a> property.




## -see-also




<a href="https://msdn.microsoft.com/11a76706-e2e5-4ae5-bdc2-5354514ea29f">Factoid Property [InkRecognizeContext Class]</a>



<a href="tablet.iinkrecognizercontext">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags Property</a>
 

 

