---
UID: NF:dmoreg.DMORegister
title: DMORegister function
author: windows-sdk-content
description: The DMORegister function registers a DMO.
old-location: dshow\dmoregister.htm
old-project: DirectShow
ms.assetid: 4e70569b-8502-4eee-bd23-173269b345d1
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: DMORegister, DMORegister function [DirectShow], dmoreg/DMORegister, dshow.dmoregister
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dmoreg.h
req.include-header: Dmo.h
req.target-type: Windows
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
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Msdmo.dll
api_name:
-	DMORegister
product: Windows
targetos: Windows
req.lib: Msdmo.lib
req.dll: Msdmo.dll
req.irql: 
---

# DMORegister function


## -description



      The <b>DMORegister</b> function registers a DMO.


## -parameters




### -param szName

NULL-terminated string that contains a descriptive name for the DMO. Names longer than 79 characters might be truncated.


### -param clsidDMO

Class identifier (CLSID) of the DMO.


### -param guidCategory


            GUID that specifies the category of the DMO. See <a href="https://msdn.microsoft.com/d67debd0-8ecb-41ab-bc6c-b27cba97c65a">DMO GUIDs</a> for a list of category GUIDs.
          


### -param dwFlags


            Bitwise combination of zero or more flags from the <a href="https://msdn.microsoft.com/472be505-a13c-4612-b799-1e9add3ee3fc">DMO_REGISTER_FLAGS</a> enumeration.

          


### -param cInTypes

Number of input media types to register. Can be zero.


### -param pInTypes


            Pointer to an array of <a href="https://msdn.microsoft.com/53bf4c34-d180-4edd-b59a-55d7d90708b5">DMO_PARTIAL_MEDIATYPE</a> structures that specify the input media types. The size of the array is specified in the cInTypes parameter
          


### -param cOutTypes

Number of output media types to register.


### -param pOutTypes

Pointer to an array of DMO_PARTIAL_MEDIATYPE structures that specify the output media types. The size of the array is specified in the cOutTypes parameter. Can be zero.


## -returns




            Returns an <b>HRESULT</b> value. Possible values include the following.

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
Failure

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Invalid argument

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>
 




## -remarks




          This function adds information about a DMO to the registry. Applications or software components can use this information to locate the DMOs they need to use, by calling the <a href="https://msdn.microsoft.com/2cb69d28-15be-44fb-a180-98b560848c08">DMOEnum</a> function. For example, to encode a video stream, you would search in the DMOCATEGORY_VIDEO_ENCODER category for a DMO whose media types matched your requirements.
        


          The media types registered by this function are only for the purpose of finding the DMO. They do not necessarily match the types returned by the <a href="https://msdn.microsoft.com/22693a22-97be-487d-ad17-31a2d8ee874c">IMediaObject::GetInputType</a> and <a href="https://msdn.microsoft.com/a7652472-4091-4ecf-b623-5c6eb01be44a">IMediaObject::GetOutputType</a> methods. For example, a decoder might register just its main input types. After the DMO is created and its input type has been set, its <b>GetOutputType</b> method will return all of the decompressed types it can generate.
        




## -see-also




<a href="https://msdn.microsoft.com/0a380dc0-23f0-4ef0-898a-3b5afddf5eaa">DMO Functions</a>
 

 

