---
UID: NF:sspi.SaslEnumerateProfilesA
title: SaslEnumerateProfilesA function
author: windows-sdk-content
description: Lists the packages that provide a SASL interface.
old-location: security\saslenumerateprofiles.htm
tech.root: secauthn
ms.assetid: 0c11e0e3-2538-4703-bc32-31c73d65a498
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: SaslEnumerateProfiles, SaslEnumerateProfiles function [Security], SaslEnumerateProfilesA, SaslEnumerateProfilesW, security.saslenumerateprofiles, sspi/SaslEnumerateProfiles, sspi/SaslEnumerateProfilesA, sspi/SaslEnumerateProfilesW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: sspi.h
req.include-header: Security.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SaslEnumerateProfilesW (Unicode) and SaslEnumerateProfilesA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Secur32.lib
req.dll: Secur32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Secur32.dll
api_name:
 - SaslEnumerateProfiles
 - SaslEnumerateProfilesA
 - SaslEnumerateProfilesW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- SaslEnumerateProfilesA
: 
---

# SaslEnumerateProfilesA function


## -description


The <b>SaslEnumerateProfiles</b> function lists the packages that provide a SASL interface.


## -parameters




### -param ProfileList [out]

Pointer to a list of Unicode or ANSI strings that contain the names of the packages with SASL wrapper support.


### -param ProfileCount [out]

Pointer to an unsigned <b>LONG</b> value that contains the number of packages with SASL wrapper support.


## -returns



If the call is completed successfully, this function returns SEC_E_OK.

If the function fails, the return value is a nonzero error code.




## -remarks



The current list is maintained in the registry under <pre xml:space="preserve"><b>SYSTEM</b>
   <b>CurrentControlSet</b>
      <b>Control</b>
         <b>SecurityProviders</b>
            <b>SaslProfiles</b></pre>


A terminating <b>NULL</b> character is appended to the end of the list.



