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

# CRYPTCATCDF_ structure


## -description


<p class="CCE_Message">[The  <b>CRYPTCATCDF</b> structure is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

The <b>CRYPTCATCDF</b> structure contains information used to create a signed catalog file (.cat) from a  catalog definition file (CDF). This structure is used by the <a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a> tool.


## -struct-fields




### -field cbStruct

The size, in bytes, of this structure.


### -field hFile

A handle to the catalog definition file (.cdf).


### -field dwCurFilePos

A value that specifies the current position of the parser measured in bytes from the beginning of the catalog definition file.


### -field dwLastMemberOffset

A value that specifies the number of bytes to the position of the last member parsed in the catalog definition file.


### -field fEOF

An integer that indicates whether the parser finished reading the file. <b>TRUE</b> indicates that the last read operation returned zero bytes.


### -field pwszResultDir

A pointer to a null-terminated string that contains the name of a directory where the catalog file (.cat) will be written.


### -field hCATStore

A handle to the catalog file (.cat).


## -remarks



A parser can update <i>dwCurFilePos</i> and <i>dwLastMemberOffset</i> as it reads the CDF. A user-defined callback function can use this information for recoverable parse errors in the CDF.




## -see-also




<a href="https://msdn.microsoft.com/9f2a1175-f9fe-4f4d-bf6f-e4f4c59739ec">CryptCATCDFClose</a>



<a href="https://msdn.microsoft.com/056a5186-a37c-4255-aaa5-4c6e60f5392e">CryptCATCDFEnumAttributesWithCDFTag</a>



<a href="https://msdn.microsoft.com/01889cb9-7bf4-4591-9bb2-b263c4effe0c">CryptCATCDFEnumCatAttributes</a>



<a href="https://msdn.microsoft.com/38e17ef2-65dc-45f8-a484-8eedcf4ce3e3">CryptCATCDFEnumMembersByCDFTagEx</a>



<a href="https://msdn.microsoft.com/d400d8bd-c0a0-41dc-9093-8e4fc758d82f">CryptCATCDFOpen</a>



<a href="https://msdn.microsoft.com/233b3644-f2a5-4166-bac0-30bf2f54e957">MakeCat</a>
 

 

