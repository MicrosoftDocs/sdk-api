---
UID: NF:wsbapp.IWsbApplicationRestoreSupport.IsRollForwardSupported
title: IWsbApplicationRestoreSupport::IsRollForwardSupported
author: windows-sdk-content
description: Reports whether the application supports roll-forward restore.
old-location: wsb\iwsbapplicationrestoresupport_isrollforwardsupported.htm
tech.root: wsb
ms.assetid: 6dae61b7-0e52-42f7-8ca4-b3566f6b4bbc
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWsbApplicationRestoreSupport interface [Windows Server Backup],IsRollForwardSupported method, IWsbApplicationRestoreSupport.IsRollForwardSupported, IWsbApplicationRestoreSupport::IsRollForwardSupported, IsRollForwardSupported, IsRollForwardSupported method [Windows Server Backup], IsRollForwardSupported method [Windows Server Backup],IWsbApplicationRestoreSupport interface, wsb.iwsbapplicationrestoresupport_isrollforwardsupported, wsbapp/IWsbApplicationRestoreSupport::IsRollForwardSupported
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsbapp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WsbApp.h
api_name:
 - IWsbApplicationRestoreSupport.IsRollForwardSupported
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsbapp.h
: 
- IWsbApplicationRestoreSupport.IsRollForwardSupported
: 
---

# IWsbApplicationRestoreSupport::IsRollForwardSupported


## -description


Reports whether the application supports roll-forward restore.


## -parameters




### -param pbRollForwardSupported [out]

Receives <b>TRUE</b> if roll-forward restore is supported, or 
      <b>FALSE</b> otherwise.


## -returns



Returns <b>S_OK</b> if successful, or an error value otherwise.




## -remarks



Applications that support roll-forward restore should set the value of the 
    <i>pbRollForwardSupported</i> parameter to <b>TRUE</b>.




## -see-also




<a href="https://msdn.microsoft.com/694f9b4d-0ca8-4dbe-829c-6ac18c9aa140">IWsbApplicationRestoreSupport</a>
 

 

