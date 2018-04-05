---
UID: NN:mbnapi.IMbnSmsReadMsgTextCdma
title: IMbnSmsReadMsgTextCdma
author: windows-driver-content
description: A collection of properties that represent a CDMA format SMS message read from the device memory.
old-location: mbn\imbnsmsreadmsgtextcdma.htm
old-project: mbn
ms.assetid: d26b09f7-eb83-46ed-82cb-a702d3af5d05
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: IMbnSmsReadMsgTextCdma, IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks], IMbnSmsReadMsgTextCdma interface [Microsoft Broadband Networks], described, mbn.imbnsmsreadmsgtextcdma, mbnapi/IMbnSmsReadMsgTextCdma
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: mbnapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Mbnapi.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MBN_VOICE_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mbnapi.h
api_name:
-	IMbnSmsReadMsgTextCdma
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMbnSmsReadMsgTextCdma interface


## -description



A collection of properties that represent a CDMA format SMS message read from the device memory.




## -remarks



This message format is valid only for CDMA devices and cannot be used with GSM devices.

 This interface is provided by the <a href="https://msdn.microsoft.com/58478c9d-6df2-466b-85bc-1c571f4429ce">OnSmsReadComplete</a> and <a href="https://msdn.microsoft.com/e6d13393-557c-462c-a640-2228ab0c9c17">OnSmsNewClass0Message</a> methods of the <a href="https://msdn.microsoft.com/06dfb631-fe5a-45d9-89f9-1f13990500ee">IMbnSmsEvents</a> interface.



