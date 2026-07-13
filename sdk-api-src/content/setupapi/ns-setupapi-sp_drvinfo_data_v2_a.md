---
UID: NS:setupapi._SP_DRVINFO_DATA_V2_A
title: SP_DRVINFO_DATA_V2_A (setupapi.h)
description: An SP_DRVINFO_DATA structure contains information about a driver. This structure is a member of a driver information list that can be associated with a particular device instance or globally with a device information set. (sp_drvinfo_data_v2_a)
helpviewer_keywords: ["*PSP_DRVINFO_DATA_V2_A","PSP_DRVINFO_DATA","PSP_DRVINFO_DATA structure pointer [Device and Driver Installation]","SP_DRVINFO_DATA","SP_DRVINFO_DATA structure [Device and Driver Installation]","SP_DRVINFO_DATA_A","SP_DRVINFO_DATA_V2","SP_DRVINFO_DATA_V2_A","devinst.sp_drvinfo_data","di-struct_738a1fa5-729a-4464-af75-05591d68eef7.xml","setupapi/PSP_DRVINFO_DATA","setupapi/SP_DRVINFO_DATA"]
old-location: devinst\sp_drvinfo_data.htm
tech.root: devinst
ms.assetid: 13cdebad-6247-4651-a1d0-709e14af22f6
ms.date: 12/05/2018
ms.keywords: '*PSP_DRVINFO_DATA_V2_A, PSP_DRVINFO_DATA, PSP_DRVINFO_DATA structure pointer [Device and Driver Installation], SP_DRVINFO_DATA, SP_DRVINFO_DATA structure [Device and Driver Installation], SP_DRVINFO_DATA_A, SP_DRVINFO_DATA_V2, SP_DRVINFO_DATA_V2_A, devinst.sp_drvinfo_data, di-struct_738a1fa5-729a-4464-af75-05591d68eef7.xml, setupapi/PSP_DRVINFO_DATA, setupapi/SP_DRVINFO_DATA'
req.header: setupapi.h
req.include-header: Setupapi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SP_DRVINFO_DATA_V2_A, *PSP_DRVINFO_DATA_V2_A
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SP_DRVINFO_DATA_V2_A
 - setupapi/_SP_DRVINFO_DATA_V2_A
 - PSP_DRVINFO_DATA_V2_A
 - setupapi/PSP_DRVINFO_DATA_V2_A
 - SP_DRVINFO_DATA_V2_A
 - setupapi/SP_DRVINFO_DATA_V2_A
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Setupapi.h
api_name:
 - SP_DRVINFO_DATA
 - sp_drvinfo_data_v2_a
---

# SP_DRVINFO_DATA_V2_A structure


## -description

An SP_DRVINFO_DATA structure contains information about a driver. This structure is a member of a driver information list that can be associated with a particular device instance or globally with a device information set.

## -struct-fields

### -field cbSize

The size, in bytes, of the SP_DRVINFO_DATA structure. For more information, see the Remarks section in this topic.

### -field DriverType

The type of driver represented by this structure. Must be one of the following values:





#### SPDIT_CLASSDRIVER

This structure represents a class driver.



#### SPDIT_COMPATDRIVER

This structure represents a compatible driver.

### -field Reserved

Reserved. For internal use only.

### -field Description

A NULL-terminated string that describes the device supported by this driver.

### -field MfgName

A NULL-terminated string that contains the name of the manufacturer of the device supported by this driver.

### -field ProviderName

A NULL-terminated string giving the provider of this driver. This is typically the name of the organization that creates the driver or INF file. <b>ProviderName</b> can be an empty string.

### -field DriverDate

Date of the driver. From the <b>DriverVer</b> entry in the INF file. See the <a href="/windows-hardware/drivers/install/inf-ddinstall-section">INF DDInstall Section</a> for more information about the <b>DriverVer</b> entry.

### -field DriverVersion

Version of the driver. From the <b>DriverVer</b> entry in the INF file.

### -field DriverType.SPDIT_CLASSDRIVER

This structure represents a class driver.

### -field DriverType.SPDIT_COMPATDRIVER

This structure represents a compatible driver.

## -remarks

In <i>SetupAPI.h</i>, this structure equates to either SP_DRVINFO_DATA_V1 or SP_DRVINFO_DATA_V2, based on whether you include the following line in your source code:


```
#define  USE_SP_DRVINFO_DATA_V1 1
```


Define this identifier only if your component must run on Windows 98 or Millennium Edition, or on Windows NT. If your component is run only in Windows 2000 and later versions of Windows, do not define the identifier. If the identifier is not defined, SP_DRVINFO_DATA_V2 is used.

SP_DRVINFO_DATA_V1 does not contain <b>DriverDate</b> and <b>DriverVersion</b> members.

<b>SetupDi</b><i>Xxx</i> functions that take an SP_DRVINFO_DATA structure as a parameter verify that the <b>cbSize</b> member of the supplied structure is equal to the size, in bytes, of the structure. If the <b>cbSize</b> member is not set correctly for an input parameter, the function will fail and set an error code of ERROR_INVALID_PARAMETER. If the <b>cbSize</b> member is not set correctly for an output parameter, the function will fail and set an error code of ERROR_INVALID_USER_BUFFER.





> [!NOTE]
> The setupapi.h header defines SP_DRVINFO_DATA_V2 as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdienumdriverinfoa">SetupDiEnumDriverInfo</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetdriverinstallparamsa">SetupDiGetDriverInstallParams</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdigetselecteddrivera">SetupDiGetSelectedDriver</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetdriverinstallparamsa">SetupDiSetDriverInstallParams</a>



<a href="/windows/desktop/api/setupapi/nf-setupapi-setupdisetselecteddrivera">SetupDiSetSelectedDriver</a>
