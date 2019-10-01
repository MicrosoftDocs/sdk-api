---
UID: NF:oaidl.IErrorInfo.GetHelpContext
title: IErrorInfo::GetHelpContext (oaidl.h)
author: windows-sdk-content
description: Returns the Help context identifier (ID) for the error.
old-location: automat\ierrorinfo_gethelpcontext.htm
tech.root: automat
ms.assetid: aadfc151-50ed-4a31-b53a-ff9d74dceb6b
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GetHelpContext, GetHelpContext method [Automation], GetHelpContext method [Automation],IErrorInfo interface, IErrorInfo interface [Automation],GetHelpContext method, IErrorInfo.GetHelpContext, IErrorInfo::GetHelpContext, _oa96_IErrorInfo_GetHelpContext, automat.ierrorinfo_gethelpcontext, oaidl/IErrorInfo::GetHelpContext
ms.topic: method
f1_keywords: 
 - "oaidl/IErrorInfo.GetHelpContext"
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - oaidl.h
api_name:
 - IErrorInfo.GetHelpContext
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IErrorInfo::GetHelpContext


## -description


Returns the Help context identifier (ID) for the error.


## -parameters




### -param pdwHelpContext [out]

The Help context ID for the error.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns the Help context ID for the error. To find the Help file to which it applies, use <a href="https://docs.microsoft.com/windows/desktop/api/oaidl/nf-oaidl-ierrorinfo-gethelpfile">IErrorInfo::GetHelpFile</a>.





## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ierrorinfo">IErrorInfo</a>
 

 

