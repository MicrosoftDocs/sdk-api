---
UID: NF:wmcontainer.IMFASFStreamPrioritization.AddStream
title: IMFASFStreamPrioritization::AddStream (wmcontainer.h)
description: Note  This interface is not implemented in this version of Media Foundation. Adds a stream to the stream priority list.
helpviewer_keywords: ["440d2838-0314-45f7-b73b-653fe5535c88","AddStream","AddStream method [Media Foundation]","AddStream method [Media Foundation]","IMFASFStreamPrioritization interface","IMFASFStreamPrioritization interface [Media Foundation]","AddStream method","IMFASFStreamPrioritization.AddStream","IMFASFStreamPrioritization::AddStream","mf.imfasfstreamprioritization_addstream","wmcontainer/IMFASFStreamPrioritization::AddStream"]
old-location: mf\imfasfstreamprioritization_addstream.htm
tech.root: mf
ms.assetid: 440d2838-0314-45f7-b73b-653fe5535c88
ms.date: 12/05/2018
ms.keywords: 440d2838-0314-45f7-b73b-653fe5535c88, AddStream, AddStream method [Media Foundation], AddStream method [Media Foundation],IMFASFStreamPrioritization interface, IMFASFStreamPrioritization interface [Media Foundation],AddStream method, IMFASFStreamPrioritization.AddStream, IMFASFStreamPrioritization::AddStream, mf.imfasfstreamprioritization_addstream, wmcontainer/IMFASFStreamPrioritization::AddStream
req.header: wmcontainer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFASFStreamPrioritization::AddStream
 - wmcontainer/IMFASFStreamPrioritization::AddStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFASFStreamPrioritization.AddStream
---

# IMFASFStreamPrioritization::AddStream


## -description

<div class="alert"><b>Note</b>  This interface is not implemented in this version of Media Foundation.</div>
<div> </div>
Adds a stream to the stream priority list.

## -parameters

### -param wStreamNumber [in]

Stream number of the stream to add.

### -param wStreamFlags [in]

If <b>TRUE</b>, the stream is mandatory.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_INVALIDREQUEST</b></dt>
</dl>
</td>
<td width="60%">
Invalid stream number.

</td>
</tr>
</table>

## -remarks

The stream priority list is built by appending entries to the list with each call to <b>AddStream</b>. The list is evaluated in descending order of importance. The most important stream should be added first, and the least important should be added last.

## -see-also

<a href="/windows/desktop/api/wmcontainer/nn-wmcontainer-imfasfstreamprioritization">IMFASFStreamPrioritization</a>