---
UID: NF:wuapi.IUpdateServiceManager.SetOption
title: IUpdateServiceManager::SetOption (wuapi.h)
description: Set options for the object that specifies the service ID. The SetOption method is also used to determine whether a warning is displayed when you change the registration of Automatic Updates.
helpviewer_keywords: ["IUpdateServiceManager interface [Windows Update Agent]","SetOption method","IUpdateServiceManager.SetOption","IUpdateServiceManager::SetOption","SetOption","SetOption method [Windows Update Agent]","SetOption method [Windows Update Agent]","IUpdateServiceManager interface","wua.iupdateservicemanager_setoption","wuapi/IUpdateServiceManager::SetOption"]
old-location: wua\iupdateservicemanager_setoption.htm
tech.root: wua
ms.assetid: dbf0b70c-5be0-4acc-9c44-bf32f6f752fd
ms.date: 12/05/2018
ms.keywords: IUpdateServiceManager interface [Windows Update Agent],SetOption method, IUpdateServiceManager.SetOption, IUpdateServiceManager::SetOption, SetOption, SetOption method [Windows Update Agent], SetOption method [Windows Update Agent],IUpdateServiceManager interface, wua.iupdateservicemanager_setoption, wuapi/IUpdateServiceManager::SetOption
req.header: wuapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP, Windows 2000 Professional with SP3 [desktop apps only]
req.target-min-winversvr: Windows Server 2003, Windows 2000 Server with SP3 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wuapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Wuguid.lib
req.dll: Wuapi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUpdateServiceManager::SetOption
 - wuapi/IUpdateServiceManager::SetOption
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wuapi.dll
api_name:
 - IUpdateServiceManager.SetOption
---

# IUpdateServiceManager::SetOption


## -description

Set options for the object that specifies the service ID. The <b>SetOption</b> method is also used to determine whether a warning is displayed when you change the registration of Automatic Updates.

## -parameters

### -param optionName [in]

Set this parameter to AllowedServiceID to specify the form of the service ID that is provided to the object. 

Set to AllowWarningUI to display a warning when changing the Automatic Updates registration.

### -param optionValue [in]

If the <i>optionName</i> parameter is set to AllowServiceID,    the <i>optionValue</i> parameter is set to the service ID that is provided as a <b>VT_BSTR</b> value.  

If <i>optionName</i> is set to AllowWarningUI,    <i>optionValue</i> is a <b>VT_BOOL</b> value that specifies whether to display a warning when changing the registration of Automatic Updates.

Set the optionValue parameter to VARIANT_TRUE to display the warning UI. Set it to VARIANT_FALSE to suppress the warning UI.

## -returns

Returns <b>S_OK</b> if successful. Otherwise, returns a COM or Windows 

error code.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WU_E_INVALID_OPERATION</b></dt>
</dl>
</td>
<td width="60%">
The computer is not allowed to access the update site.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An argument of the method is invalid.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/wuapi/nn-wuapi-iupdateservicemanager">IUpdateServiceManager</a>