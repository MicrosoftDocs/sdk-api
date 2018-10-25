---
UID: NF:msinkaut.IInkRecognizerContext.IsStringSupported
title: IInkRecognizerContext::IsStringSupported
author: windows-sdk-content
description: Indicates whether the system dictionary, user dictionary, or word list contain a specified string.
old-location: tablet\inkrecognizercontext_isstringsupported.htm
tech.root: tablet
ms.assetid: 5344044a-0973-4ab2-bf5c-74e0d07d4e76
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: 5344044a-0973-4ab2-bf5c-74e0d07d4e76, IInkRecognizerContext interface [Tablet PC],IsStringSupported method, IInkRecognizerContext.IsStringSupported, IInkRecognizerContext::IsStringSupported, IsStringSupported, IsStringSupported method [Tablet PC], IsStringSupported method [Tablet PC],IInkRecognizerContext interface, msinkaut/IInkRecognizerContext::IsStringSupported, tablet.inkrecognizercontext_isstringsupported
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: InkObj.dll
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - InkObj.dll
 - InkObj.dll.dll
api_name:
 - IInkRecognizerContext.IsStringSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInkRecognizerContext::IsStringSupported


## -description



Indicates whether the system dictionary, user dictionary, or <a href="https://msdn.microsoft.com/d189fd13-ec69-45dc-8be4-fea48f337636">word list</a> contain a specified string.




## -parameters




### -param String

TBD


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



<a href="https://msdn.microsoft.com/D3DC08E9-19CC-4281-9C71-CB9B8CBDDB7F">IInkRecognizerContext</a>



<a href="https://msdn.microsoft.com/2b39fd32-831d-4606-8600-b52aaa7ed882">InkRecognizerContext Class</a>



<a href="https://msdn.microsoft.com/71b02f99-4076-4c56-b88a-4201b7033411">RecognitionFlags Property</a>
 

 

