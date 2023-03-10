---
UID: NF:oaidl.ICreateErrorInfo.SetHelpFile
title: ICreateErrorInfo::SetHelpFile (oaidl.h)
description: Sets the path of the Help file that describes the error.
helpviewer_keywords: ["ICreateErrorInfo interface [Automation]","SetHelpFile method","ICreateErrorInfo.SetHelpFile","ICreateErrorInfo::SetHelpFile","SetHelpFile","SetHelpFile method [Automation]","SetHelpFile method [Automation]","ICreateErrorInfo interface","_oa96_ICreateErrorInfo_SetHelpFile","automat.icreateerrorinfo_sethelpfile","oaidl/ICreateErrorInfo::SetHelpFile"]
old-location: automat\icreateerrorinfo_sethelpfile.htm
tech.root: automat
ms.assetid: bb439d74-fd52-4c95-afc5-d57e2fe5029d
ms.date: 12/05/2018
ms.keywords: ICreateErrorInfo interface [Automation],SetHelpFile method, ICreateErrorInfo.SetHelpFile, ICreateErrorInfo::SetHelpFile, SetHelpFile, SetHelpFile method [Automation], SetHelpFile method [Automation],ICreateErrorInfo interface, _oa96_ICreateErrorInfo_SetHelpFile, automat.icreateerrorinfo_sethelpfile, oaidl/ICreateErrorInfo::SetHelpFile
req.header: oaidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OaIdl.idl
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
 - ICreateErrorInfo::SetHelpFile
 - oaidl/ICreateErrorInfo::SetHelpFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - ICreateErrorInfo.SetHelpFile
---

# ICreateErrorInfo::SetHelpFile


## -description

Sets the path of the Help file that describes the error.

## -parameters

### -param szHelpFile [in]

The fully qualified path of the Help file that describes the error.

## -returns

This method can return one of these values.

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
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.


</td>
</tr>
</table>

## -remarks

This method sets the fully qualified path of the Help file that describes the current error. Use <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-icreateerrorinfo-sethelpcontext">ICreateErrorInfo::SetHelpContext</a> to set the Help context ID for the error in the Help file.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-icreateerrorinfo">ICreateErrorInfo</a>