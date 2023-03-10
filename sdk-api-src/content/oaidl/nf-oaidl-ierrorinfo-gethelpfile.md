---
UID: NF:oaidl.IErrorInfo.GetHelpFile
title: IErrorInfo::GetHelpFile (oaidl.h)
description: Returns the path of the Help file that describes the error.
helpviewer_keywords: ["GetHelpFile","GetHelpFile method [Automation]","GetHelpFile method [Automation]","IErrorInfo interface","IErrorInfo interface [Automation]","GetHelpFile method","IErrorInfo.GetHelpFile","IErrorInfo::GetHelpFile","_oa96_IErrorInfo_GetHelpFile","automat.ierrorinfo_gethelpfile","oaidl/IErrorInfo::GetHelpFile"]
old-location: automat\ierrorinfo_gethelpfile.htm
tech.root: automat
ms.assetid: f8458382-0af7-4a9b-add3-9c99af070be4
ms.date: 12/05/2018
ms.keywords: GetHelpFile, GetHelpFile method [Automation], GetHelpFile method [Automation],IErrorInfo interface, IErrorInfo interface [Automation],GetHelpFile method, IErrorInfo.GetHelpFile, IErrorInfo::GetHelpFile, _oa96_IErrorInfo_GetHelpFile, automat.ierrorinfo_gethelpfile, oaidl/IErrorInfo::GetHelpFile
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
 - IErrorInfo::GetHelpFile
 - oaidl/IErrorInfo::GetHelpFile
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
 - IErrorInfo.GetHelpFile
---

# IErrorInfo::GetHelpFile


## -description

Returns the path of the Help file that describes the error.

## -parameters

### -param pBstrHelpFile [out]

The fully qualified path of the Help file.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method returns the fully qualified path of the Help file that describes the current error. <a href="/previous-versions/windows/desktop/api/oaidl/nf-oaidl-ierrorinfo-gethelpcontext">IErrorInfo::GetHelpContext</a> should be used to find the Help context ID for the error in the Help file.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>