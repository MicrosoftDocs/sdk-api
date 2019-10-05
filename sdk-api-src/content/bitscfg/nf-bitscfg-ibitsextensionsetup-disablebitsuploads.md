---
UID: NF:bitscfg.IBITSExtensionSetup.DisableBITSUploads
title: IBITSExtensionSetup::DisableBITSUploads (bitscfg.h)
author: windows-sdk-content
description: Use the DisableBITSUploads method to disable BITS upload on the virtual directory to which the ADSI object points. This method sets the BITSUploadEnabled IIS extension property.
old-location: bits\ibitsextensionsetup_disablebitsuploads.htm
tech.root: Bits
ms.assetid: 3d439054-a751-4f63-9e82-223d1ce9c551
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DisableBITSUploads, DisableBITSUploads method [BITS], DisableBITSUploads method [BITS],IBITSExtensionSetup interface, IBITSExtensionSetup interface [BITS],DisableBITSUploads method, IBITSExtensionSetup.DisableBITSUploads, IBITSExtensionSetup::DisableBITSUploads, _drz_ibitsextensionsetup_disablebitsuploads, bits.ibitsextensionsetup_disablebitsuploads, bitscfg/IBITSExtensionSetup::DisableBITSUploads
ms.topic: method
f1_keywords: 
 - "bitscfg/IBITSExtensionSetup.DisableBITSUploads"
dev_langs:
 - c++
req.header: bitscfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2003
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bitscfg.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetup.DisableBITSUploads
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on Windows XP
ms.custom: 19H1
---

# IBITSExtensionSetup::DisableBITSUploads


## -description


Use the 
<b>DisableBITSUploads</b> method to disable BITS upload on the virtual directory to which the ADSI object points. This method sets the 
<a href="https://docs.microsoft.com/windows/desktop/Bits/bits-iis-extension-properties">BITSUploadEnabled</a> IIS extension property.


## -parameters






## -returns



This method returns <b>S_OK</b> for success. Otherwise, the method failed.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads">IBITSExtensionSetup::EnableBITSUploads</a>
 

 

