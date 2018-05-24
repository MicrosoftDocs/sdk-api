---
UID: NF:oaidl.IErrorInfo.GetHelpFile
title: IErrorInfo::GetHelpFile
author: windows-driver-content
description: Returns the path of the Help file that describes the error.
old-location: automat\ierrorinfo_gethelpfile.htm
old-project: automat
ms.assetid: f8458382-0af7-4a9b-add3-9c99af070be4
ms.author: windowsdriverdev
ms.date: 5/4/2018
ms.keywords: GetHelpFile, GetHelpFile method [Automation], GetHelpFile method [Automation],IErrorInfo interface, IErrorInfo interface [Automation],GetHelpFile method, IErrorInfo.GetHelpFile, IErrorInfo::GetHelpFile, _oa96_IErrorInfo_GetHelpFile, automat.ierrorinfo_gethelpfile, oaidl/IErrorInfo::GetHelpFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: VARKIND
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	oaidl.h
api_name:
-	IErrorInfo.GetHelpFile
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IErrorInfo::GetHelpFile


## -description


Returns the path of the Help file that describes the error.


## -parameters




### -param pBstrHelpFile [out]

The fully qualified path of the Help file.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method returns the fully qualified path of the Help file that describes the current error. <a href="https://msdn.microsoft.com/aadfc151-50ed-4a31-b53a-ff9d74dceb6b">IErrorInfo::GetHelpContext</a> should be used to find the Help context ID for the error in the Help file.





## -see-also




<a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a>
 

 

