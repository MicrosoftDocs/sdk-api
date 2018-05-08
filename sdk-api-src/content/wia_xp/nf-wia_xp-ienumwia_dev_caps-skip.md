---
UID: NF:wia_xp.IEnumWIA_DEV_CAPS.Skip
title: IEnumWIA_DEV_CAPS::Skip
author: windows-driver-content
description: The IEnumWIA_DEV_CAPS::Skip method skips the specified number of hardware device capabilities during an enumeration of available device capabilities.
old-location: wia\_wia_IEnumWIA_DEV_CAPS_Skip.htm
old-project: wia
ms.assetid: VS|wia|~\wia\refwia\ifaces\ienumwia_dev_caps\skip.htm
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: IEnumWIA_DEV_CAPS interface [WIA],Skip method, IEnumWIA_DEV_CAPS.Skip, IEnumWIA_DEV_CAPS::Skip, Skip, Skip method [WIA], Skip method [WIA],IEnumWIA_DEV_CAPS interface, _wia_IEnumWIA_DEV_CAPS_Skip, wia._wia_IEnumWIA_DEV_CAPS_Skip, wia_xp/IEnumWIA_DEV_CAPS::Skip
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
-	IEnumWIA_DEV_CAPS.Skip
product: Windows
targetos: Windows
req.lib: Wiaguid.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# IEnumWIA_DEV_CAPS::Skip


## -description


The <b>IEnumWIA_DEV_CAPS::Skip</b> method skips the specified number of hardware device capabilities during an enumeration of available device capabilities.



## -parameters




### -param celt [in]

Type: <b>ULONG</b>

Specifies the number of items to skip. 


## -returns



Type: <b>HRESULT</b>

If the method succeeds, the method returns S_OK. It returns S_FALSE if it could not skip the specified number of device capabilities. If the method fails, it returns a standard COM error code.



