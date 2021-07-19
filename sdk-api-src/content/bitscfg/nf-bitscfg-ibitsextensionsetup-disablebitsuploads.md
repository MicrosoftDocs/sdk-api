---
UID: NF:bitscfg.IBITSExtensionSetup.DisableBITSUploads
title: IBITSExtensionSetup::DisableBITSUploads (bitscfg.h)
description: Use the DisableBITSUploads method to disable BITS upload on the virtual directory to which the ADSI object points. This method sets the BITSUploadEnabled IIS extension property.
helpviewer_keywords: ["DisableBITSUploads","DisableBITSUploads method [BITS]","DisableBITSUploads method [BITS]","IBITSExtensionSetup interface","IBITSExtensionSetup interface [BITS]","DisableBITSUploads method","IBITSExtensionSetup.DisableBITSUploads","IBITSExtensionSetup::DisableBITSUploads","_drz_ibitsextensionsetup_disablebitsuploads","bits.ibitsextensionsetup_disablebitsuploads","bitscfg/IBITSExtensionSetup::DisableBITSUploads"]
old-location: bits\ibitsextensionsetup_disablebitsuploads.htm
tech.root: Bits
ms.assetid: 3d439054-a751-4f63-9e82-223d1ce9c551
ms.date: 12/05/2018
ms.keywords: DisableBITSUploads, DisableBITSUploads method [BITS], DisableBITSUploads method [BITS],IBITSExtensionSetup interface, IBITSExtensionSetup interface [BITS],DisableBITSUploads method, IBITSExtensionSetup.DisableBITSUploads, IBITSExtensionSetup::DisableBITSUploads, _drz_ibitsextensionsetup_disablebitsuploads, bits.ibitsextensionsetup_disablebitsuploads, bitscfg/IBITSExtensionSetup::DisableBITSUploads
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
targetos: Windows
req.typenames: 
req.redist: BITS 1.5 on Windows XP
ms.custom: 19H1
f1_keywords:
 - IBITSExtensionSetup::DisableBITSUploads
 - bitscfg/IBITSExtensionSetup::DisableBITSUploads
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - BitsMgr.dll
api_name:
 - IBITSExtensionSetup.DisableBITSUploads
---

# IBITSExtensionSetup::DisableBITSUploads


## -description

Use the 
<b>DisableBITSUploads</b> method to disable BITS upload on the virtual directory to which the ADSI object points. This method sets the 
<a href="/windows/desktop/Bits/bits-iis-extension-properties">BITSUploadEnabled</a> IIS extension property.



## -returns

This method returns <b>S_OK</b> for success. Otherwise, the method failed.

## -see-also

<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-enablebitsuploads">IBITSExtensionSetup::EnableBITSUploads</a>
