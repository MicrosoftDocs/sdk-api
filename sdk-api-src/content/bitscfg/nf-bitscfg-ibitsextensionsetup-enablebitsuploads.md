---
UID: NF:bitscfg.IBITSExtensionSetup.EnableBITSUploads
title: IBITSExtensionSetup::EnableBITSUploads (bitscfg.h)
description: Use the EnableBITSUploads method to enable BITS upload on the virtual directory to which the ADSI object points. This method sets the BITSUploadEnabled IIS extension property.
helpviewer_keywords: ["EnableBITSUploads","EnableBITSUploads method [BITS]","EnableBITSUploads method [BITS]","IBITSExtensionSetup interface","IBITSExtensionSetup interface [BITS]","EnableBITSUploads method","IBITSExtensionSetup.EnableBITSUploads","IBITSExtensionSetup::EnableBITSUploads","_drz_ibitsextensionsetup_enablebitsuploads","bits.ibitsextensionsetup_enablebitsuploads","bitscfg/IBITSExtensionSetup::EnableBITSUploads"]
old-location: bits\ibitsextensionsetup_enablebitsuploads.htm
tech.root: Bits
ms.assetid: 5b68dea2-f9a7-4a99-93d3-62c4f24b769f
ms.date: 12/05/2018
ms.keywords: EnableBITSUploads, EnableBITSUploads method [BITS], EnableBITSUploads method [BITS],IBITSExtensionSetup interface, IBITSExtensionSetup interface [BITS],EnableBITSUploads method, IBITSExtensionSetup.EnableBITSUploads, IBITSExtensionSetup::EnableBITSUploads, _drz_ibitsextensionsetup_enablebitsuploads, bits.ibitsextensionsetup_enablebitsuploads, bitscfg/IBITSExtensionSetup::EnableBITSUploads
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
 - IBITSExtensionSetup::EnableBITSUploads
 - bitscfg/IBITSExtensionSetup::EnableBITSUploads
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
 - IBITSExtensionSetup.EnableBITSUploads
---

# IBITSExtensionSetup::EnableBITSUploads


## -description

Use the 
<b>EnableBITSUploads</b> method to enable BITS upload on the virtual directory to which the ADSI object points. This method sets the 
<a href="/windows/desktop/Bits/bits-iis-extension-properties">BITSUploadEnabled</a> IIS extension property.



## -returns

This method returns <b>S_OK</b> for success. Otherwise, the method failed.

## -remarks

This method turns off the scripting and execute permissions on the virtual directory; you cannot upload files to a virtual directory that has scripting and execute permissions enabled. If the permissions are restored after calling this method, the upload jobs fail with an error code of <b>BG_E_SERVER_EXECUTE_ENABLED</b>.

The 
<b>EnableBITSUploads</b> method fails if the <a href="/windows/desktop/TaskSchd/task-scheduler-start-page">Task Scheduler</a> is disabled.


#### Examples

See the example for the 
<a href="/windows/desktop/api/bitscfg/nn-bitscfg-ibitsextensionsetup">IBITSExtensionSetup</a> interface.

<div class="code"></div>

## -see-also

<a href="/windows/desktop/api/bitscfg/nf-bitscfg-ibitsextensionsetup-disablebitsuploads">IBITSExtensionSetup::DisableBITSUploads</a>
