---
UID: NF:bitscfg.IBITSExtensionSetup.DisableBITSUploads
title: IBITSExtensionSetup::DisableBITSUploads method
author: windows-driver-content
description: Use the DisableBITSUploads method to disable BITS upload on the virtual directory to which the ADSI object points. This method sets the BITSUploadEnabled IIS extension property.
old-location: bits\ibitsextensionsetup_disablebitsuploads.htm
old-project: Bits
ms.assetid: 3d439054-a751-4f63-9e82-223d1ce9c551
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: DisableBITSUploads method [BITS], DisableBITSUploads method [BITS], IBITSExtensionSetup interface, DisableBITSUploads,IBITSExtensionSetup.DisableBITSUploads, IBITSExtensionSetup, IBITSExtensionSetup interface [BITS], DisableBITSUploads method, IBITSExtensionSetup::DisableBITSUploads, _drz_ibitsextensionsetup_disablebitsuploads, bits.ibitsextensionsetup_disablebitsuploads, bitscfg/IBITSExtensionSetup::DisableBITSUploads
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: BITS_FILE_PROPERTY_VALUE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	BitsMgr.dll
api_name:
-	IBITSExtensionSetup.DisableBITSUploads
product: Windows
targetos: Windows
req.lib: 
req.dll: BitsMgr.dll
req.irql: 
---

# IBITSExtensionSetup::DisableBITSUploads method


## -description


Use the 
<b>DisableBITSUploads</b> method to disable BITS upload on the virtual directory to which the ADSI object points. This method sets the 
<a href="https://msdn.microsoft.com/08a40cc1-ec6d-4b65-971a-15c7b06df148">BITSUploadEnabled</a> IIS extension property.


## -parameters






## -returns



This method returns <b>S_OK</b> for success. Otherwise, the method failed.




## -see-also




<a href="https://msdn.microsoft.com/5b68dea2-f9a7-4a99-93d3-62c4f24b769f">IBITSExtensionSetup::EnableBITSUploads</a>
 

 

