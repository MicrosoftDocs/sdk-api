---
UID: NF:imapi2.IDiscFormat2Data.get_LastWrittenAddressOfPreviousSession
title: IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession (imapi2.h)
description: Retrieves the last sector of the previous write session.
helpviewer_keywords: ["IDiscFormat2Data interface [IMAPI]","get_LastWrittenAddressOfPreviousSession method","IDiscFormat2Data.get_LastWrittenAddressOfPreviousSession","IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession","get_LastWrittenAddressOfPreviousSession","get_LastWrittenAddressOfPreviousSession method [IMAPI]","get_LastWrittenAddressOfPreviousSession method [IMAPI]","IDiscFormat2Data interface","imapi.idiscformat2data_get_lastwrittenaddressofprevioussession","imapi2/IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession"]
old-location: imapi\idiscformat2data_get_lastwrittenaddressofprevioussession.htm
tech.root: imapi
ms.assetid: cfc9ba42-25a2-49a3-8047-7aaf331332ad
ms.date: 12/05/2018
ms.keywords: IDiscFormat2Data interface [IMAPI],get_LastWrittenAddressOfPreviousSession method, IDiscFormat2Data.get_LastWrittenAddressOfPreviousSession, IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession, get_LastWrittenAddressOfPreviousSession, get_LastWrittenAddressOfPreviousSession method [IMAPI], get_LastWrittenAddressOfPreviousSession method [IMAPI],IDiscFormat2Data interface, imapi.idiscformat2data_get_lastwrittenaddressofprevioussession, imapi2/IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession
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
 - IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession
 - imapi2/IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession
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
 - IDiscFormat2Data.get_LastWrittenAddressOfPreviousSession
---

# IDiscFormat2Data::get_LastWrittenAddressOfPreviousSession


## -description

Retrieves the last sector of the previous write session.

## -parameters

### -param value [out]

  Address where the previous write operation ended.  

The value is -1 if the media is blank or does not support multi-session writing (indicates that no previous session could be detected).

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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Not implemented.

Value: 0x80004001

</td>
</tr>
</table>

## -remarks

<div class="alert"><b>Note</b>  This property should not be used. Instead, you should use an interface derived from <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisession">IMultisession</a>, such as <a href="/windows/desktop/api/imapi2/nn-imapi2-imultisessionsequential">IMultisessionSequential</a>, for importing file data from the previous session.</div>
<div> </div>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2data">IDiscFormat2Data</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_nextwritableaddress">IDiscFormat2Data::get_NextWritableAddress</a>



<a href="/windows/desktop/api/imapi2/nf-imapi2-idiscformat2data-get_startaddressofprevioussession">IDiscFormat2Data::get_StartAddressOfPreviousSession</a>