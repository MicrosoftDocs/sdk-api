---
UID: NF:wiamdef.CWiaLogProcEx.CWiaLogProcEx
title: CWiaLogProcEx::CWiaLogProcEx method
author: windows-driver-content
description: The CWiaLogProcEx constructor is called when the function or method being logged is entered.
old-location: image\cwialogprocex_cwialogprocex.htm
old-project: image
ms.assetid: D4004501-2DA5-416C-A29B-C0084CF34DC9
ms.author: windowsdriverdev
ms.date: 2/27/2018
ms.keywords: CWiaLogProcEx, CWiaLogProcEx interface [Imaging Devices], CWiaLogProcEx method, CWiaLogProcEx method [Imaging Devices], CWiaLogProcEx method [Imaging Devices], CWiaLogProcEx interface, CWiaLogProcEx,CWiaLogProcEx.CWiaLogProcEx, CWiaLogProcEx::CWiaLogProcEx, image.cwialogprocex_cwialogprocex, wiamdef/CWiaLogProcEx::CWiaLogProcEx
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wiamdef.h
req.include-header: Wiamdef.h
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WER_RUNTIME_EXCEPTION_INFORMATION, *PWER_RUNTIME_EXCEPTION_INFORMATION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wiamdef.h
api_name:
-	CWiaLogProcEx.CWiaLogProcEx
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# CWiaLogProcEx::CWiaLogProcEx method


## -description


The <a href="https://msdn.microsoft.com/5DD3EC13-5DDD-4640-A841-00576F74429A">CWiaLogProcEx</a> constructor is called when the function or method being logged is entered.


## -parameters




### -param pIWiaLog




### -param ResourceID

Defines the <b>INT</b> parameter <i>ResourceID</i>.


### -param DetailLevel

Defines the <b>INT</b> parameter <i>DetailLevel</i>.


### -param pszMsg




### -param lMethodId






#### - *pIWiaLogEx

Defines the <b>IWiaLogEx</b> parameter <i>*pIWiaLog</i>.


#### - *pszMsg

Defines the <b>CHAR</b> parameter <i>*pszMsg</i>.


#### - lMethodId = 0

Defines the <b>LONG</b> parameter <i>lMethodId</i>.


## -returns



This method does not return a value.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/windows/hardware/mt844723">CWiaLogProcEx</a>
 

 

