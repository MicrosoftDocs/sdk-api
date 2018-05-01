---
UID: NF:wia_xp.IEnumWIA_DEV_INFO.Skip
title: IEnumWIA_DEV_INFO::Skip method
author: windows-driver-content
description: The IEnumWIA_DEV_INFO::Skip method skips the specified number of hardware devices during an enumeration of available devices.
old-location: wia\_wia_IEnumWIA_DEV_INFO_Skip.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_dev_info\skip.htm
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IEnumWIA_DEV_INFO, IEnumWIA_DEV_INFO interface [WIA], Skip method, IEnumWIA_DEV_INFO::Skip, Skip method [WIA], Skip method [WIA], IEnumWIA_DEV_INFO interface, Skip,IEnumWIA_DEV_INFO.Skip, _wia_IEnumWIA_DEV_INFO_Skip, wia._wia_IEnumWIA_DEV_INFO_Skip, wia_xp/IEnumWIA_DEV_INFO::Skip
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: WIAVIDEO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiaguid.lib
-	Wiaguid.dll
api_name:
-	IEnumWIA_DEV_INFO.Skip
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWIA_DEV_INFO::Skip method


## -description


The <b>IEnumWIA_DEV_INFO::Skip</b> method skips the specified number of hardware devices during an enumeration of available devices.


## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of devices to skip.


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the method returns S_OK. If it is unable to skip the specified number of devices, it returns S_FALSE. If the method fails, it returns a standard COM error code.



