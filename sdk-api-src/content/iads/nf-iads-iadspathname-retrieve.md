---
UID: NF:iads.IADsPathname.Retrieve
title: IADsPathname::Retrieve
author: windows-sdk-content
description: The IADsPathname::Retrieve method retrieves the path of the object with different format types.
old-location: adsi\iadspathname_retrieve.htm
tech.root: adsi
ms.assetid: c34f2a5e-5faf-45bf-acc6-8db5fc8bf5fa
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IADsPathname interface [ADSI],Retrieve method, IADsPathname.Retrieve, IADsPathname::Retrieve, Retrieve, Retrieve method [ADSI], Retrieve method [ADSI],IADsPathname interface, _ds_iadspathname_retrieve, adsi.iadspathname__retrieve, adsi.iadspathname_retrieve, iads/IADsPathname::Retrieve
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Activeds.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsPathname.Retrieve
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IADsPathname::Retrieve


## -description


The <b>IADsPathname::Retrieve</b> method retrieves the path of the object with different format types.


## -parameters




### -param lnFormatType [in]

Specifies the format that the path should be retrieved in. This can be one of the values specified in the <a href="https://msdn.microsoft.com/d0c94f30-6b8c-4c7a-bb74-205b2b658dbb">ADS_FORMAT_ENUM</a> enumeration.


### -param pbstrADsPath [out]

Contains a pointer to a <b>BSTR</b> value the receives the object path. The caller must free this memory with the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function when it is no longer required.


## -returns



This method supports the standard return values, as well as the following.

For more information and other return values, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/d0c94f30-6b8c-4c7a-bb74-205b2b658dbb">ADS_FORMAT_ENUM</a>



<a href="https://msdn.microsoft.com/9aa26d6c-aa86-4a23-a986-b8cb9057772a">IADsPathname</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

