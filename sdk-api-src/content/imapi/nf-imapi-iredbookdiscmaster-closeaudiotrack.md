---
UID: NF:imapi.IRedbookDiscMaster.CloseAudioTrack
title: IRedbookDiscMaster::CloseAudioTrack method
author: windows-driver-content
description: Closes a currently open audio track. All audio tracks must be closed before the IDiscMaster::RecordDisc method can be called.
old-location: imapi\iredbookdiscmaster_closeaudiotrack.htm
old-project: imapi
ms.assetid: 01ec0eba-d592-46eb-8029-86cb678b8b34
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: CloseAudioTrack method [IMAPI], CloseAudioTrack method [IMAPI], IRedbookDiscMaster interface, CloseAudioTrack,IRedbookDiscMaster.CloseAudioTrack, IRedbookDiscMaster, IRedbookDiscMaster interface [IMAPI], CloseAudioTrack method, IRedbookDiscMaster::CloseAudioTrack, _win32_iredbookdiscmaster_closeaudiotrack, base.iredbookdiscmaster_closeaudiotrack, imapi.iredbookdiscmaster_closeaudiotrack, imapi/IRedbookDiscMaster::CloseAudioTrack
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: imapi.h
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
req.typenames: AM_LINE21_DRAWBGMODE, *PAM_LINE21_DRAWBGMODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Actxprxy.dll
api_name:
-	IRedbookDiscMaster.CloseAudioTrack
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
req.product: GDI+ 1.1
---

# IRedbookDiscMaster::CloseAudioTrack method


## -description


Closes a currently open audio track. All audio tracks must be closed before the 
<a href="https://msdn.microsoft.com/2b234dc5-2409-49d8-83be-0ffea74f5bcf">IDiscMaster::RecordDisc</a> method can be called.


## -parameters






## -returns



S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:




## -see-also




<a href="https://msdn.microsoft.com/ea531b22-869a-400e-801f-00bb85ebaac2">IRedbookDiscMaster</a>
 

 

