---
UID: NN:imapi.IJolietDiscMaster
title: IJolietDiscMaster (imapi.h)
description: The IJolietDiscMaster interface enables the staging of a CD data disc.
helpviewer_keywords: ["IJolietDiscMaster","IJolietDiscMaster interface [IMAPI]","IJolietDiscMaster interface [IMAPI]","described","_win32_ijolietdiscmaster","base.ijolietdiscmaster","imapi.ijolietdiscmaster","imapi/IJolietDiscMaster"]
old-location: imapi\ijolietdiscmaster.htm
tech.root: imapi
ms.assetid: e2269b68-1860-4afd-90f2-d61297f3fa9b
ms.date: 12/05/2018
ms.keywords: IJolietDiscMaster, IJolietDiscMaster interface [IMAPI], IJolietDiscMaster interface [IMAPI],described, _win32_ijolietdiscmaster, base.ijolietdiscmaster, imapi.ijolietdiscmaster, imapi/IJolietDiscMaster
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
req.lib: Uuid.lib
req.dll: Actxprxy.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IJolietDiscMaster
 - imapi/IJolietDiscMaster
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Actxprxy.dll
api_name:
 - IJolietDiscMaster
---

# IJolietDiscMaster interface


## -description

The 
<b>IJolietDiscMaster</b> interface enables the staging of a CD data disc. It represents one of the formats supported by <b>MSDiscMasterObj</b>, and it allows the creation of a single Track-at-Once data disc. The data is written to the disc with the Joliet and ISO-9660 file systems.

A temporary folder is constructed and added to the image. This can be repeated multiple times with the directory and file structures overlapping. The overlapping file structures appear seamlessly when read back. When the overwrite option is used, overlapping paths cause the last file added to show up in the directory, while the earlier files with conflicting names are still present on the disc but now not readable by normal means.

## -inheritance

The <b>IJolietDiscMaster</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IJolietDiscMaster</b> also has these types of members:

