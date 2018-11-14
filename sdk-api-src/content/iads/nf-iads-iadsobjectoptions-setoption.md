---
UID: NF:iads.IADsObjectOptions.SetOption
title: IADsObjectOptions::SetOption
author: windows-sdk-content
description: Sets a provider-specific option for manipulating a directory object.
old-location: adsi\iadsobjectoptions_setoption.htm
tech.root: ADSI
ms.assetid: e6e43c99-fc8b-4f34-82cf-8cf30c506859
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IADsObjectOptions interface [ADSI],SetOption method, IADsObjectOptions.SetOption, IADsObjectOptions::SetOption, SetOption, SetOption method [ADSI], SetOption method [ADSI],IADsObjectOptions interface, _ds_iadsobjectoptions_setoption, adsi.iadsobjectoptions__setoption, adsi.iadsobjectoptions_setoption, iads/IADsObjectOptions::SetOption
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
 - IADsObjectOptions.SetOption
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- iads.h
: 
- IADsObjectOptions.SetOption
: 
---

# IADsObjectOptions::SetOption


## -description


The <b>IADsOptions.SetOption</b> method sets a provider-specific option for manipulating a directory object.


## -parameters




### -param lnOption

Indicates the provider-specific option to set. This parameter can be any value in the  <a href="https://msdn.microsoft.com/afb32e03-7e4e-4df9-87c7-db962d62e5f0">ADS_OPTION_ENUM</a> enumeration except <b>ADS_OPTION_SERVERNAME</b> or <b>ADS_OPTION_MUTUAL_AUTH_STATUS</b>.


### -param vValue

Specifies the value to set for the option specified in the <i>lnOption</i> parameter.


## -returns



The method supports the standard return values, including <b>S_OK</b> for a successful operation and <b>E_ADS_BAD_PARAMETER</b> when the user has supplied an invalid <i>pValue</i> parameter. For more information, see  <a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/573889e4-37af-4aca-afd7-ef06bcf8aa0d">ADSI Error Codes</a>



<a href="https://msdn.microsoft.com/1884efe5-86f5-4579-a25e-2ff9c9a6ec2a">IADsObjectOptions</a>
 

 

