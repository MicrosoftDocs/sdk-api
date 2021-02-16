---
UID: NF:imapi2fs.IBootOptions.put_Emulation
title: IBootOptions::put_Emulation (imapi2fs.h)
description: Sets the media type that the boot image is intended to emulate.
helpviewer_keywords: ["IBootOptions interface [IMAPI]","put_Emulation method","IBootOptions.put_Emulation","IBootOptions::put_Emulation","imapi.ibootoptions_put_emulation","imapi2fs/IBootOptions::put_Emulation","put_Emulation","put_Emulation method [IMAPI]","put_Emulation method [IMAPI]","IBootOptions interface"]
old-location: imapi\ibootoptions_put_emulation.htm
tech.root: imapi
ms.assetid: 93ed301e-fdea-451c-9ab0-6ea9a7fd45de
ms.date: 12/05/2018
ms.keywords: IBootOptions interface [IMAPI],put_Emulation method, IBootOptions.put_Emulation, IBootOptions::put_Emulation, imapi.ibootoptions_put_emulation, imapi2fs/IBootOptions::put_Emulation, put_Emulation, put_Emulation method [IMAPI], put_Emulation method [IMAPI],IBootOptions interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBootOptions::put_Emulation
 - imapi2fs/IBootOptions::put_Emulation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IBootOptions.put_Emulation
---

# IBootOptions::put_Emulation


## -description

Sets the media type that the boot image is intended to emulate.

## -parameters

### -param newVal [in]

Media type that the boot image is intended to emulate. For possible values, see the <a href="/windows/desktop/api/imapi2fs/ne-imapi2fs-emulationtype">EmulationType</a> enumeration type. The default value is <b>EmulationNone</b>, which means the BIOS will not emulate any device type or special sector size for the CD during boot from the CD.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation. The following error codes are commonly returned on operation failure, but do not represent the only possible error values:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>IMAPI_E_BOOT_EMULATION_IMAGE_SIZE_MISMATCH</b></dt>
</dl>
</td>
<td width="60%">
The emulation type requested does not match the boot image size.

Value: 0xC0AAB14A

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2fs/nn-imapi2fs-ibootoptions">IBootOptions</a>



<a href="/windows/desktop/api/imapi2fs/nf-imapi2fs-ibootoptions-get_emulation">IBootOptions::get_Emulation</a>