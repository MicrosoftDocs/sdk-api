---
UID: NF:imapi2.IRawCDImageCreator.put_StartOfLeadoutLimit
title: IRawCDImageCreator::put_StartOfLeadoutLimit (imapi2.h)
description: Sets the StartOfLeadoutLimit property value.
helpviewer_keywords: ["IRawCDImageCreator interface [IMAPI]","put_StartOfLeadoutLimit method","IRawCDImageCreator.put_StartOfLeadoutLimit","IRawCDImageCreator::put_StartOfLeadoutLimit","imapi.irawcdimagecreator_put_startofleadoutlimit","imapi2/IRawCDImageCreator::put_StartOfLeadoutLimit","put_StartOfLeadoutLimit","put_StartOfLeadoutLimit method [IMAPI]","put_StartOfLeadoutLimit method [IMAPI]","IRawCDImageCreator interface"]
old-location: imapi\irawcdimagecreator_put_startofleadoutlimit.htm
tech.root: imapi
ms.assetid: e3483084-8339-4fe6-abd1-832832c549f3
ms.date: 12/05/2018
ms.keywords: IRawCDImageCreator interface [IMAPI],put_StartOfLeadoutLimit method, IRawCDImageCreator.put_StartOfLeadoutLimit, IRawCDImageCreator::put_StartOfLeadoutLimit, imapi.irawcdimagecreator_put_startofleadoutlimit, imapi2/IRawCDImageCreator::put_StartOfLeadoutLimit, put_StartOfLeadoutLimit, put_StartOfLeadoutLimit method [IMAPI], put_StartOfLeadoutLimit method [IMAPI],IRawCDImageCreator interface
req.header: imapi2.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2.idl
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
 - IRawCDImageCreator::put_StartOfLeadoutLimit
 - imapi2/IRawCDImageCreator::put_StartOfLeadoutLimit
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2.h
api_name:
 - IRawCDImageCreator.put_StartOfLeadoutLimit
---

# IRawCDImageCreator::put_StartOfLeadoutLimit


## -description

Sets the <i>StartOfLeadoutLimit</i> property value. This value specifies if the resulting image is required to fit on a piece of media with a <b>StartOfLeadout</b> greater than or equal to the LBA specified.<div class="alert"><b>Note</b>  The maximum supported value for this property is 398,099, which equates to MSF 88:29:74. </div>
<div> </div>

## -parameters

### -param value [in]

Pointer to a <b>LONG</b> value that represents the current  <i>StartOfLeadoutLimit</i>.

## -returns

S_OK is returned on success, but other success codes may be returned as a result of implementation.

## -remarks

This method is supported in Windows Server 2003 with Service Pack 1 (SP1), Windows XP with Service Pack 2 (SP2),  and Windows Vista  via the Windows Feature Pack for Storage. All  features provided by this  update package are supported natively in Windows 7 and Windows Server 2008 R2.

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-irawcdimagecreator">IRawCDImageCreator</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-irawcdimagecreator-get_startofleadoutlimit">IRawCDImageCreator::get_StartOfLeadoutLimit</a>