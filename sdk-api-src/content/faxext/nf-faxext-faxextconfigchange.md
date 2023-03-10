---
UID: NF:faxext.FaxExtConfigChange
title: FaxExtConfigChange function (faxext.h)
description: A FaxExtConfigChange callback function is a placeholder for a function name defined by the fax extension DLL. The fax extension DLL should not expose this function.
helpviewer_keywords: ["FaxExtConfigChange","FaxExtConfigChange function [Fax Service]","_mfax_faxextconfigchange","fax._mfax_faxextconfigchange","faxext/FaxExtConfigChange"]
old-location: fax\_mfax_faxextconfigchange.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxextconfigref_4azp.htm
ms.date: 12/05/2018
ms.keywords: FaxExtConfigChange, FaxExtConfigChange function [Fax Service], _mfax_faxextconfigchange, fax._mfax_faxextconfigchange, faxext/FaxExtConfigChange
req.header: faxext.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FaxExtConfigChange
 - faxext/FaxExtConfigChange
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - FaxExt.h
api_name:
 - FaxExtConfigChange
---

# FaxExtConfigChange function


## -description

A <b>FaxExtConfigChange</b> callback function is a placeholder for a function name defined by the fax extension DLL. The fax extension DLL should not expose this function.

## -parameters

### -param dwDeviceId [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> value that indicates the device for which the configuration data has changed.




This parameter can be zero, indicating a change in the extension's global configuration data (configuration data that is not associated with a specific device). For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-storing-global-configuration-data">Storing Global Configuration Data</a>.

### -param lpcwstrDataGUID [in]

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the GUID of the data that has changed; for example, "{b8959fc9-4e77-4ee9-8411-009acb1bbf3e}".

### -param lpData [in]

Type: <b>LPBYTE</b>

Pointer to a buffer that contains the new configuration data.

### -param dwDataSize [in]

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> value that indicates the size, in bytes, of the buffer pointed to by the <i>lpData</i> parameter.

## -returns

Type: <b>HRESULT</b>

If the function succeeds, the return value is of the type <b>HRESULT</b>, and the value is <b>NOERROR</b>.

## -remarks

The fax service calls this function after a change in device configuration data occurs. The fax service calls this function only if the fax extension has registered to receive notifications about configuration changes by calling the <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextregisterforevents">FaxExtRegisterForEvents</a> function.

If an extension registers to receive notifications about changes in configuration data, that extension does not receive notifications about new configuration values it sets itself. You can change a device's configuration data by calling the	<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextsetdata">FaxExtSetData</a> function. 

The fax extension DLL must register the <b>FaxExtConfigChange</b> callback function by passing its address to the <a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextregisterforevents">FaxExtRegisterForEvents</a> callback function. The PFAX_EXT_CONFIG_CHANGE data type is a pointer to a <b>FaxExtConfigChange</b> function.

## -see-also

<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextregisterforevents">FaxExtRegisterForEvents</a>



<a href="/previous-versions/windows/desktop/api/faxext/nf-faxext-faxextsetdata">FaxExtSetData</a>