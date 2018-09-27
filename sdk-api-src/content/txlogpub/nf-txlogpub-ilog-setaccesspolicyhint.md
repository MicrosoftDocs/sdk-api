---
UID: NF:txlogpub.ILog.SetAccessPolicyHint
title: ILog::SetAccessPolicyHint
author: windows-sdk-content
description: Provides a hint to the implementation about the pattern in which records will be read.
old-location: com\ilog_setaccesspolicyhint.htm
tech.root: com
ms.assetid: a0a34300-e5de-4e47-9c61-389272283b61
ms.author: windowssdkdev
ms.date: 09/25/2018
ms.keywords: ILog interface [COM],SetAccessPolicyHint method, ILog.SetAccessPolicyHint, ILog::SetAccessPolicyHint, SetAccessPolicyHint, SetAccessPolicyHint method [COM], SetAccessPolicyHint method [COM],ILog interface, _com_ilog_setaccesspolicyhint, com.ilog_setaccesspolicyhint, txlogpub/ILog::SetAccessPolicyHint
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: txlogpub.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Txlogpub.idl
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
 - Txlogpub.h
api_name:
 - ILog.SetAccessPolicyHint
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILog::SetAccessPolicyHint


## -description


Provides a hint to the implementation about the pattern in which records will be read.


## -parameters




### -param policy [in]

The pattern in which records will most often be read. For more information, see the <a href="https://msdn.microsoft.com/79ffd37a-ffeb-46f8-8743-aa3e85648e34">RECORD_READING_POLICY</a> enumeration.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Not all implementations of <a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a> will be optimized for reading records in a particular pattern. An implementation may choose to ignore this request and return S_OK.




## -see-also




<a href="https://msdn.microsoft.com/93f2be99-0799-4047-ae4e-62f0e74d15c3">ILog</a>



<a href="https://msdn.microsoft.com/79ffd37a-ffeb-46f8-8743-aa3e85648e34">RECORD_READING_POLICY</a>
 

 

