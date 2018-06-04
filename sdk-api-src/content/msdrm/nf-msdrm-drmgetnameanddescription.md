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

# DRMGetNameAndDescription function


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGetNameAndDescription</b> function retrieves a language specific name and description from an issuance license.


## -parameters




### -param hIssuanceLicense [in]

A handle to the issuance license to get the information from.


### -param uIndex [in]

The zero-based index of the name and description pair to retrieve.


### -param pulcid [out]

A pointer to a <b>UINT</b> that receives the locale ID of the name and description pair.


### -param puNameLength [in, out]

A pointer to a <b>UINT</b> that, on input, contains the length, in characters, of the <i>wszName</i> buffer. This length must include the terminating null character.

After the function returns, this <b>UINT</b> contains the number of characters, including the terminating null character, that were copied to the <i>wszName</i> buffer.


### -param wszName [out]

A pointer to a null-terminated Unicode string that receives the name. The size of this buffer is specified by the <i>puNameLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puNameLength</i> parameter.


### -param puDescriptionLength [in, out]

A pointer to a <b>UINT</b> that, on input, contains the length, in characters, of the <i>wszDescription</i> buffer. This length must include the terminating null character.

After the function returns, this <b>UINT</b> contains the number of characters, including the terminating null character, that were copied to the <i>wszDescription</i> buffer.


### -param wszDescription [out]

A pointer to a null-terminated Unicode string that receives the description. The size of this buffer is specified by the <i>puDescriptionLength</i> parameter.

To determine the required size of this buffer, pass <b>NULL</b> for this parameter. The function will place the size, in characters, including the terminating null character, in the <i>puDescriptionLength</i> parameter.


## -returns



If the function succeeds, the function returns S_OK.

If the function fails, it returns an <b>HRESULT</b> value that indicates the error. Possible values include, but are not limited to, those in the following list. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -remarks



<div class="alert"><b>Note</b>  If, when you enumerate through the Name/Description pairs for locales, you are unable to find the Name/Description pair corresponding with your locale (using the locale ID), you can use the LCID of 0, which is the  default value. Take note that an LCID of 0  can be set only for templates and licenses created programmatically on the client. AD RMS server administration does not support setting a default language for Name and Description. For more information about creating an issuance license programmatically, see   <a href="https://msdn.microsoft.com/495024be-5d97-4869-99f7-b68efb9e8039">Creating an Issuance License</a>.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/b3b4e7c6-d3d3-4bf7-b6c4-9502a56a7223">AD RMS Functions</a>



<a href="https://msdn.microsoft.com/c5dc8aa8-f45b-4b8a-bd83-0661db424303">DRMSetNameAndDescription</a>
 

 

