---
UID: NF:gpedit.IRSOPInformation.GetFlags
title: IRSOPInformation::GetFlags
author: windows-driver-content
description: The GetFlags method retrieves information about the RSoP user interface session.
old-location: policy\irsopinformation_getflags.htm
old-project: Policy
ms.assetid: 10a518a3-9097-4efd-90cc-14ea66b70fa2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetFlags, GetFlags method [Group Policy], GetFlags method [Group Policy],IRSOPInformation interface, IRSOPInformation interface [Group Policy],GetFlags method, IRSOPInformation.GetFlags, IRSOPInformation::GetFlags, RSOP_INFO_FLAG_LOGGING_MODE, _win32_irsopinformation_getflags, gpedit/IRSOPInformation::GetFlags, policy.irsopinformation_getflags
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Gpedit.dll
api_name:
-	IRSOPInformation.GetFlags
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IRSOPInformation::GetFlags


## -description


The
    <b>GetFlags</b> method retrieves information about the RSoP user interface session.


## -parameters




### -param pdwFlags [out]

Receives a pointer to a value that contains information about the RSoP session. This parameter can be the following value.



#### RSOP_INFO_FLAG_LOGGING_MODE

If this value is specified, the RSoP session is in logging mode. If this value is not specified, it indicates that the session is in planning mode.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/e3662977-d7a7-47bc-989b-a820d4c05382">IRSOPInformation</a>
 

 

