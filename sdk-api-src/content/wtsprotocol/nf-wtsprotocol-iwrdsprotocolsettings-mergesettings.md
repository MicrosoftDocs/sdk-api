---
UID: NF:wtsprotocol.IWRdsProtocolSettings.MergeSettings
title: IWRdsProtocolSettings::MergeSettings (wtsprotocol.h)
description: Adds (merges) the specified policy-related settings into the larger group of connection settings.
helpviewer_keywords: ["IWRdsProtocolSettings interface [Remote Desktop Services]","MergeSettings method","IWRdsProtocolSettings.MergeSettings","IWRdsProtocolSettings::MergeSettings","MergeSettings","MergeSettings method [Remote Desktop Services]","MergeSettings method [Remote Desktop Services]","IWRdsProtocolSettings interface","termserv.iwrdsprotocolsettings_mergesettings","wtsprotocol/IWRdsProtocolSettings::MergeSettings"]
old-location: termserv\iwrdsprotocolsettings_mergesettings.htm
tech.root: TermServ
ms.assetid: fa05bcde-e4db-481b-88ab-57d070153517
ms.date: 12/05/2018
ms.keywords: IWRdsProtocolSettings interface [Remote Desktop Services],MergeSettings method, IWRdsProtocolSettings.MergeSettings, IWRdsProtocolSettings::MergeSettings, MergeSettings, MergeSettings method [Remote Desktop Services], MergeSettings method [Remote Desktop Services],IWRdsProtocolSettings interface, termserv.iwrdsprotocolsettings_mergesettings, wtsprotocol/IWRdsProtocolSettings::MergeSettings
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
 - IWRdsProtocolSettings::MergeSettings
 - wtsprotocol/IWRdsProtocolSettings::MergeSettings
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
 - IWRdsProtocolSettings.MergeSettings
---

# IWRdsProtocolSettings::MergeSettings


## -description

Adds (merges) the specified policy-related settings into the larger group of connection settings.

## -parameters

### -param pWRdsSettings [in]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_settings">WRDS_SETTINGS</a> structure that contains the policy-related settings to add.

### -param WRdsConnectionSettingLevel [in]

A value of the <a href="/windows/desktop/api/wtsdefs/ne-wtsdefs-wrds_connection_setting_level">WRDS_CONNECTION_SETTING_LEVEL</a> enumeration that specifies the type of structure contained in the <b>WRdsConnectionSetting</b> member of the <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings">WRDS_CONNECTION_SETTINGS</a> structure.

### -param pWRdsConnectionSettings [in, out]

A pointer to a <a href="/windows/desktop/api/wtsdefs/ns-wtsdefs-wrds_connection_settings">WRDS_CONNECTION_SETTINGS</a> structure that contains the existing connection settings. When the method returns, this structure is updated to include the merged settings.

## -returns

When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="/windows/desktop/SecCrypto/common-hresult-values">Common HRESULT Values</a>.

## -see-also

<a href="/windows/desktop/api/wtsprotocol/nn-wtsprotocol-iwrdsprotocolsettings">IWRdsProtocolSettings</a>