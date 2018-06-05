---
UID: NF:mfobjects.IMFAttributes.GetAllocatedString
title: IMFAttributes::GetAllocatedString
author: windows-sdk-content
description: Gets a wide-character string associated with a key. This method allocates the memory for the string.
old-location: mf\imfattributes_getallocatedstring.htm
old-project: medfound
ms.assetid: 550a3035-ea16-4784-8f69-9522259bb338
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: 550a3035-ea16-4784-8f69-9522259bb338, GetAllocatedString, GetAllocatedString method [Media Foundation], GetAllocatedString method [Media Foundation],IMFAttributes interface, IMFAttributes interface [Media Foundation],GetAllocatedString method, IMFAttributes.GetAllocatedString, IMFAttributes::GetAllocatedString, mf.imfattributes_getallocatedstring, mfobjects/IMFAttributes::GetAllocatedString
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
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
req.typenames: MF_FILE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFAttributes.GetAllocatedString
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFAttributes::GetAllocatedString


## -description



          Gets a wide-character string associated with a key. This method allocates the memory for the string.
        


## -parameters




### -param guidKey [in]

A GUID that identifies which value to retrieve. The attribute type must be <b>MF_ATTRIBUTE_STRING</b>.
          


### -param ppwszValue [out]

If the key is found and the value is a string type, this parameter receives a copy of the string. The caller must free the memory for the string by calling <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.
          


### -param pcchLength [out]


            Receives the number of characters in the string, excluding the terminating <b>NULL</b> character. This parameter must not be <b>NULL</b>.
          


## -returns




            The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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

                The method succeeded.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_ATTRIBUTENOTFOUND</b></dt>
</dl>
</td>
<td width="60%">

                The specified key was not found.
              

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDTYPE</b></dt>
</dl>
</td>
<td width="60%">

                The attribute value is not a string.
              

</td>
</tr>
</table>
 




## -remarks



To copy a string value into a caller-allocated buffer, use the <a href="https://msdn.microsoft.com/756d8fba-d372-46f9-8035-f657d7ff133f">IMFAttributes::GetString</a> method.

This interface is available on the following platforms if the Windows Media Format 11 SDK redistributable components are installed:

<ul>
<li>Windows XP with Service Pack 2 (SP2) and later.</li>
<li>Windows XP Media Center Edition 2005 with KB900325 (Windows XP Media Center Edition 2005) and KB925766 (October 2006 Update Rollup for Windows XP Media Center Edition) installed.</li>
</ul>
<div class="alert"><b>Note</b>  An earlier version of the documentation incorrectly stated that the <i>pcchLength</i> parameter can be <b>NULL</b>. Setting this parameter to <b>NULL</b> might succeed in some cases, but is not guaranteed. The caller must pass a non-<b>NULL</b> pointer for this parameter.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/44af5e03-5f0a-4564-b9d6-b8c935df35b2">Attributes and Properties</a>



<a href="https://msdn.microsoft.com/e12259f4-b631-4d4a-a296-c1cc6334b962">IMFAttributes</a>



<a href="https://msdn.microsoft.com/1844fbe2-0a07-4c0c-9ffe-4c59fc01f793">MF_ATTRIBUTE_TYPE</a>
 

 

