---
UID: NF:faxcomex.IFaxOutgoingJob.Pause
title: IFaxOutgoingJob::Pause
author: windows-sdk-content
description: The IFaxOutgoingJob::Pause method pauses the outbound fax job.
old-location: fax\_mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_pause_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_7ijp.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxOutgoingJob interface [Fax Service],Pause method, IFaxOutgoingJob.Pause, IFaxOutgoingJob::Pause, Pause, Pause method [Fax Service], Pause method [Fax Service],IFaxOutgoingJob interface, _mfax_faxoutgoingjob.pause, fax._mfax_faxoutgoingjob_cpp_mfax_faxoutgoingjob_pause_cpp, fax._mfax_faxoutgoingjob_pause, faxcomex/IFaxOutgoingJob::Pause
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
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
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxOutgoingJob.Pause
 - IFaxOutgoingJob.Pause
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxOutgoingJob::Pause


## -description


The <b>IFaxOutgoingJob::Pause</b> method pauses the outbound fax job.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Use the <a href="https://msdn.microsoft.com/2893d8fc-0d11-4a78-9b67-a37c43b58955">IFaxOutgoingJob::Resume</a> method to resume a fax job after it has been paused.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farSUBMIT_LOW</a> or <b>farMANAGE_JOBS</b> access right. With the <b>farSUBMIT_LOW</b> access right, users will be able to use this method only for their own faxes. With the <b>farMANAGE_JOBS</b> access right, users will be able to use this method for all faxes on the server.




## -see-also




<a href="https://msdn.microsoft.com/3b7c9ecb-0528-4cda-9c9a-cb31e4589c71">IFaxOutgoingJob</a>
 

 

