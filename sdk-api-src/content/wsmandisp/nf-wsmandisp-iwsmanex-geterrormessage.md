---
UID: NF:wsmandisp.IWSManEx.GetErrorMessage
title: IWSManEx::GetErrorMessage
author: windows-sdk-content
description: Returns a formatted string containing the text of an error number.
old-location: winrm\iwsmanex_geterrormessage.htm
tech.root: WinRM
ms.assetid: af5ae515-458a-4d7f-80f8-0fd51f97e7f1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: GetErrorMessage, GetErrorMessage method [Windows Remote Management], GetErrorMessage method [Windows Remote Management],IWSManEx interface, IWSManEx interface [Windows Remote Management],GetErrorMessage method, IWSManEx.GetErrorMessage, IWSManEx::GetErrorMessage, winrm.iwsmanex_geterrormessage, wsmandisp/IWSManEx::GetErrorMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsmandisp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: WSManDisp.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WSManDisp.tlb
req.dll: WSMAuto.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - WSMAuto.dll
api_name:
 - IWSManEx.GetErrorMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsmandisp.h
: 
- IWSManEx.GetErrorMessage
: 
---

# IWSManEx::GetErrorMessage


## -description


Returns a formatted string containing the text of an error number. This method performs the same operation as the <b>Winrm</b> command-line <b>winrm helpmsg </b><i>error number</i>. 


## -parameters




### -param errorNumber [in]

Error message number in decimal or hexadecimal from WinRM, WinHTTP, or other operating system components.


### -param errorMessage [out]

Error message string formatted like messages returned from the  <b>Winrm</b> command.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The corresponding scripting method is <a href="https://msdn.microsoft.com/5f0a5259-8356-4406-8612-34f4921184f0">WSMan.GetErrorMessage</a>.




## -see-also




<a href="https://msdn.microsoft.com/23fdd9d9-4a78-4c01-8e5d-c8007f39d5d6">IWSManEx</a>



<a href="https://msdn.microsoft.com/3e016080-339f-4bda-bfd2-f912e090981f">IWSManSession</a>
 

 

