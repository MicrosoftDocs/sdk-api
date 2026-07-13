---
UID: NF:wia_xp.IEnumWIA_FORMAT_INFO.Skip
title: IEnumWIA_FORMAT_INFO::Skip (wia_xp.h)
description: The IEnumWIA_FORMAT_INFO::Skip method skips the specified number of structures in the enumeration.
helpviewer_keywords: ["IEnumWIA_FORMAT_INFO interface [WIA]","Skip method","IEnumWIA_FORMAT_INFO.Skip","IEnumWIA_FORMAT_INFO::Skip","Skip","Skip method [WIA]","Skip method [WIA]","IEnumWIA_FORMAT_INFO interface","_wia_IEnumWIA_FORMAT_INFO_Skip","wia._wia_IEnumWIA_FORMAT_INFO_Skip","wia_xp/IEnumWIA_FORMAT_INFO::Skip"]
old-location: wia\_wia_IEnumWIA_FORMAT_INFO_Skip.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_format_info\skip.htm
ms.date: 12/05/2018
ms.keywords: IEnumWIA_FORMAT_INFO interface [WIA],Skip method, IEnumWIA_FORMAT_INFO.Skip, IEnumWIA_FORMAT_INFO::Skip, Skip, Skip method [WIA], Skip method [WIA],IEnumWIA_FORMAT_INFO interface, _wia_IEnumWIA_FORMAT_INFO_Skip, wia._wia_IEnumWIA_FORMAT_INFO_Skip, wia_xp/IEnumWIA_FORMAT_INFO::Skip
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
 - IEnumWIA_FORMAT_INFO::Skip
 - wia_xp/IEnumWIA_FORMAT_INFO::Skip
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
 - IEnumWIA_FORMAT_INFO.Skip
archived: true
---

# IEnumWIA_FORMAT_INFO::Skip


## -description

The <b>IEnumWIA_FORMAT_INFO::Skip</b> method skips the specified number of structures in the enumeration.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of structures to skip.

## -returns

Type: <b>HRESULT</b>

This method returns S_OK if it is able to skip the specified number of elements. It returns S_FALSE if it is unable to skip the specified number of elements. If the method fails, it returns a standard COM error.

