---
UID: NF:mdmregistration.GetManagementAppHyperlink
title: GetManagementAppHyperlink function (mdmregistration.h)
description: Retrieves the management app hyperlink associated with the MDM service.
old-location: mdmreg\getmanagementapphyperlink.htm
tech.root: MDMReg
ms.assetid: e319dd2e-3d2b-4c65-9b59-cd4aab930f12
ms.date: 12/05/2018
ms.keywords: GetManagementAppHyperlink, GetManagementAppHyperlink function [MDM Registration], mdmreg.getmanagementapphyperlink, mdmregistration/GetManagementAppHyperlink
ms.topic: function
f1_keywords:
- mdmregistration/GetManagementAppHyperlink
dev_langs:
- c++
req.header: mdmregistration.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1
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
req.lib: MDMRegistration.lib
req.dll: MDMRegistration.dll
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- MDMRegistration.dll
api_name:
- GetManagementAppHyperlink
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# GetManagementAppHyperlink function


## -description


Retrieves the management app hyperlink associated with the MDM service.


## -parameters




### -param cchHyperlink [in]

Contains the maximum length that can be returned through the <i>pszHyperlink</i> 
      parameter.


### -param pszHyperlink

Address of a buffer that receives the <b>NULL</b>-terminated Unicode string with the 
      hyperlink of the management app associated with the management service.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>. If the function 
      fails, the returned value describes the error. Possible values include those listed at 
      <a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>.




## -remarks



The caller of this function must be running as an elevated process.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-constants">MDM Registration Error Values</a>



<a href="https://docs.microsoft.com/windows/desktop/MDMReg/mdm-registration-functions">MDM Registration Functions</a>
 

 

