---
UID: NF:wia_xp.IEnumWIA_FORMAT_INFO.Next
title: IEnumWIA_FORMAT_INFO::Next (wia_xp.h)
description: The IEnumWIA_FORMAT_INFO::Next method returns an array of WIA_FORMAT_INFO structures.
helpviewer_keywords: ["IEnumWIA_FORMAT_INFO interface [WIA]","Next method","IEnumWIA_FORMAT_INFO.Next","IEnumWIA_FORMAT_INFO::Next","Next","Next method [WIA]","Next method [WIA]","IEnumWIA_FORMAT_INFO interface","_wia_IEnumWIA_FORMAT_INFO_Next","wia._wia_IEnumWIA_FORMAT_INFO_Next","wia_xp/IEnumWIA_FORMAT_INFO::Next"]
old-location: wia\_wia_IEnumWIA_FORMAT_INFO_Next.htm
tech.root: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_format_info\next.htm
ms.date: 12/05/2018
ms.keywords: IEnumWIA_FORMAT_INFO interface [WIA],Next method, IEnumWIA_FORMAT_INFO.Next, IEnumWIA_FORMAT_INFO::Next, Next, Next method [WIA], Next method [WIA],IEnumWIA_FORMAT_INFO interface, _wia_IEnumWIA_FORMAT_INFO_Next, wia._wia_IEnumWIA_FORMAT_INFO_Next, wia_xp/IEnumWIA_FORMAT_INFO::Next
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
 - IEnumWIA_FORMAT_INFO::Next
 - wia_xp/IEnumWIA_FORMAT_INFO::Next
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
 - IEnumWIA_FORMAT_INFO.Next
archived: true
---

# IEnumWIA_FORMAT_INFO::Next


## -description

The <b>IEnumWIA_FORMAT_INFO::Next</b> method returns an array of <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a> structures.

## -parameters

### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of elements requested.

### -param rgelt [out]

Type: <b><a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a>*</b>

Receives the address of the array of <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a> structures.

### -param pceltFetched [in, out]

Type: <b>ULONG*</b>

On output, receives the address of a <b>ULONG</b> that contains the number of <a href="/windows/desktop/api/wia_xp/ns-wia_xp-wia_format_info">WIA_FORMAT_INFO</a> structures actually returned in the <i>rgelt</i> parameter.

## -returns

Type: <b>HRESULT</b>

If the enumeration is continuing, this method returns S_OK and sets the value pointed to by <i>pceltFetched</i> to the number of capabilities returned. If the enumeration is complete, it returns S_FALSE and sets the value pointed to by <i>pceltFetched</i> to zero. If the method fails, it returns a standard COM error.