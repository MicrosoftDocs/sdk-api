---
UID: NF:wtsprotocol.IWRdsProtocolSettings.GetSettings
title: IWRdsProtocolSettings::GetSettings (wtsprotocol.h)
description: Retrieves the settings for a particular policy.
helpviewer_keywords: ["GetSettings","GetSettings method [Remote Desktop Services]","GetSettings method [Remote Desktop Services]","IWRdsProtocolSettings interface","IWRdsProtocolSettings interface [Remote Desktop Services]","GetSettings method","IWRdsProtocolSettings.GetSettings","IWRdsProtocolSettings::GetSettings","termserv.iwrdsprotocolsettings_getsettings","wtsprotocol/IWRdsProtocolSettings::GetSettings"]
old-location: termserv\iwrdsprotocolsettings_getsettings.htm
tech.root: TermServ
ms.assetid: 3a5a7ffd-15e1-4313-ad44-e720cd260f02
ms.date: 12/05/2018
ms.keywords: GetSettings, GetSettings method [Remote Desktop Services], GetSettings method [Remote Desktop Services],IWRdsProtocolSettings interface, IWRdsProtocolSettings interface [Remote Desktop Services],GetSettings method, IWRdsProtocolSettings.GetSettings, IWRdsProtocolSettings::GetSettings, termserv.iwrdsprotocolsettings_getsettings, wtsprotocol/IWRdsProtocolSettings::GetSettings
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
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
 - IWRdsProtocolSettings::GetSettings
 - wtsprotocol/IWRdsProtocolSettings::GetSettings
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wtsprotocol.h
api_name:
 - IWRdsProtocolSettings.GetSettings
---

# IWRdsProtocolSettings::GetSettings


## -description

Retrieves the settings for a particular policy.

## -parameters

### -param WRdsSettingType [in]

A value of the <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wrds_setting_type">WRDS_SETTING_TYPE</a> enumeration that specifies the area in which to retrieve the settings (machine group policy, user group policy, or user security accounts manager).

### -param WRdsSettingLevel [in]

A value of the <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wrds_setting_level">WRDS_SETTING_LEVEL</a> enumeration that specifies the type of structure contained in the <b>WRdsSetting</b> member of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings">WRDS_SETTINGS</a> structure.

### -param pWRdsSettings [out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings">WRDS_SETTINGS</a> structure that contains the returned settings.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings">IWRdsProtocolSettings</a>