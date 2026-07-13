---
UID: NF:sspi.SaslEnumerateProfilesW
title: SaslEnumerateProfilesW function (sspi.h)
description: Lists the packages that provide a SASL interface. (Unicode)
helpviewer_keywords: ["SaslEnumerateProfiles", "SaslEnumerateProfiles function [Security]", "SaslEnumerateProfilesW", "security.saslenumerateprofiles", "sspi/SaslEnumerateProfiles", "sspi/SaslEnumerateProfilesW"]
old-location: security\saslenumerateprofiles.htm
tech.root: security
ms.assetid: 0c11e0e3-2538-4703-bc32-31c73d65a498
ms.date: 12/05/2018
ms.keywords: SaslEnumerateProfiles, SaslEnumerateProfiles function [Security], SaslEnumerateProfilesA, SaslEnumerateProfilesW, security.saslenumerateprofiles, sspi/SaslEnumerateProfiles, sspi/SaslEnumerateProfilesA, sspi/SaslEnumerateProfilesW
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SaslEnumerateProfilesW
 - sspi/SaslEnumerateProfilesW
dev_langs:
 - c++
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
---

# SaslEnumerateProfilesW function


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

The current list is maintained in the registry under <pre><b>SYSTEM</b>
   <b>CurrentControlSet</b>
      <b>Control</b>
         <b>SecurityProviders</b>
            <b>SaslProfiles</b></pre>


A terminating <b>NULL</b> character is appended to the end of the list.




> [!NOTE]
> The sspi.h header defines SaslEnumerateProfiles as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

