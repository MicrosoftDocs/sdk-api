---
UID: NF:wia_xp.IEnumWIA_DEV_INFO.Skip
title: IEnumWIA_DEV_INFO::Skip (wia_xp.h)
description: The IEnumWIA_DEV_INFO::Skip method skips the specified number of hardware devices during an enumeration of available devices.
helpviewer_keywords: ["IEnumWIA_DEV_INFO interface [WIA]","Skip method","IEnumWIA_DEV_INFO.Skip","IEnumWIA_DEV_INFO::Skip","Skip","Skip method [WIA]","Skip method [WIA]","IEnumWIA_DEV_INFO interface","_wia_IEnumWIA_DEV_INFO_Skip","wia._wia_IEnumWIA_DEV_INFO_Skip","wia_xp/IEnumWIA_DEV_INFO::Skip"]
old-location: wia\_wia_IEnumWIA_DEV_INFO_Skip.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_dev_info\skip.htm
ms.date: 12/05/2018
ms.keywords: IEnumWIA_DEV_INFO interface [WIA],Skip method, IEnumWIA_DEV_INFO.Skip, IEnumWIA_DEV_INFO::Skip, Skip, Skip method [WIA], Skip method [WIA],IEnumWIA_DEV_INFO interface, _wia_IEnumWIA_DEV_INFO_Skip, wia._wia_IEnumWIA_DEV_INFO_Skip, wia_xp/IEnumWIA_DEV_INFO::Skip
req.header: wia_xp.h
req.include-header: Wia.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
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
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumWIA_DEV_INFO::Skip
 - wia_xp/IEnumWIA_DEV_INFO::Skip
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wiaguid.lib
 - Wiaguid.dll
api_name:
 - IEnumWIA_DEV_INFO.Skip
archived: true
---

# IEnumWIA_DEV_INFO::Skip


## -description

The <b>IEnumWIA_DEV_INFO::Skip</b> method skips the specified number of hardware devices during an enumeration of available devices.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of devices to skip.

## -returns

Type: <b>HRESULT</b>

If the method succeeds, the method returns S_OK. If it is unable to skip the specified number of devices, it returns S_FALSE. If the method fails, it returns a standard COM error code.

