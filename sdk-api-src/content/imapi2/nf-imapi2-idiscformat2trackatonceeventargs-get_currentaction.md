---
UID: NF:imapi2.IDiscFormat2TrackAtOnceEventArgs.get_CurrentAction
title: IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction (imapi2.h)
description: Retrieves the current write action being performed. (IDiscFormat2TrackAtOnceEventArgs.get_CurrentAction)
helpviewer_keywords: ["IDiscFormat2TrackAtOnceEventArgs interface [IMAPI]","get_CurrentAction method","IDiscFormat2TrackAtOnceEventArgs.get_CurrentAction","IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction","get_CurrentAction","get_CurrentAction method [IMAPI]","get_CurrentAction method [IMAPI]","IDiscFormat2TrackAtOnceEventArgs interface","imapi.idiscformat2trackatonceeventargs_get_currentaction","imapi2/IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction"]
old-location: imapi\idiscformat2trackatonceeventargs_get_currentaction.htm
tech.root: imapi
ms.assetid: c4a0a07a-c80e-4dca-b3bb-8b2f26f969d8
ms.date: 12/05/2018
ms.keywords: IDiscFormat2TrackAtOnceEventArgs interface [IMAPI],get_CurrentAction method, IDiscFormat2TrackAtOnceEventArgs.get_CurrentAction, IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction, get_CurrentAction, get_CurrentAction method [IMAPI], get_CurrentAction method [IMAPI],IDiscFormat2TrackAtOnceEventArgs interface, imapi.idiscformat2trackatonceeventargs_get_currentaction, imapi2/IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction
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
 - IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction
 - imapi2/IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction
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
 - IDiscFormat2TrackAtOnceEventArgs.get_CurrentAction
---

# IDiscFormat2TrackAtOnceEventArgs::get_CurrentAction


## -description

Retrieves the current write action being performed.

## -parameters

### -param value [out]

Current write action being performed. For a list of possible actions, see  the <a href="/windows/desktop/api/imapi2/ne-imapi2-imapi_format2_tao_write_action">IMAPI_FORMAT2_TAO_WRITE_ACTION</a> enumeration type.

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
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
Pointer is not valid.

Value: 0x80004003

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/imapi2/nn-imapi2-ddiscformat2trackatonceevents">DDiscFormat2TrackAtOnceEvents</a>



<a href="/windows/desktop/api/imapi2/nn-imapi2-idiscformat2trackatonceeventargs">IDiscFormat2TrackAtOnceEventArgs</a>
