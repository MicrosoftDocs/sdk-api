---
UID: NF:iads.IADsObjectOptions.GetOption
title: IADsObjectOptions::GetOption
author: windows-sdk-content
description: Gets a provider-specific option for a directory object.
old-location: adsi\iadsobjectoptions_getoption.htm
old-project: ADSI
ms.assetid: 77a994d2-81ae-4afb-be5c-be8d7159a2c2
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: GetOption, GetOption method [ADSI], GetOption method [ADSI],IADsObjectOptions interface, IADsObjectOptions interface [ADSI],GetOption method, IADsObjectOptions.GetOption, IADsObjectOptions::GetOption, _ds_iadsobjectoptions_getoption, adsi.iadsobjectoptions__getoption, adsi.iadsobjectoptions_getoption, iads/IADsObjectOptions::GetOption
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ADS_SD_FORMAT_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsObjectOptions.GetOption
product: Windows
targetos: Windows
req.lib: 
req.dll: Activeds.dll
req.irql: 
req.product: GDI+ 1.1
---

# IADsObjectOptions::GetOption


## -description


The <b>IADsOptions.GetOption</b> method gets a provider-specific option for a directory object.


## -parameters




### -param lnOption

Indicates the provider-specific option to get. This parameter can be any value in the  <a href="https://msdn.microsoft.com/afb32e03-7e4e-4df9-87c7-db962d62e5f0">ADS_OPTION_ENUM</a> enumeration.


### -param pvValue

Pointer to a <b>VARIANT</b> variable that receives the current value for the option specified in the <i>lnOption</i> parameter.


## -returns



The method supports the standard return values, including <b>S_OK</b> if the operation is successful, and <b>E_ADS_BAD_PARAMETER</b> if the user has supplied an invalid <i>pvValue</i> parameter. For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/afb32e03-7e4e-4df9-87c7-db962d62e5f0">ADS_OPTION_ENUM</a>



<a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a>
 

 

