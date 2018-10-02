---
UID: NF:faxcomex.IFaxIncomingArchive.GetMessage
title: IFaxIncomingArchive::GetMessage
author: windows-sdk-content
description: The GetMessage method returns a fax message from the archive of inbound faxes by using the fax message ID.
old-location: fax\_mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessage_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_223p.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetMessage, GetMessage method [Fax Service], GetMessage method [Fax Service],IFaxIncomingArchive interface, IFaxIncomingArchive interface [Fax Service],GetMessage method, IFaxIncomingArchive.GetMessage, IFaxIncomingArchive::GetMessage, _mfax_faxincomingarchive.getmessage, fax._mfax_faxincomingarchive_cpp_mfax_faxincomingarchive_getmessage_cpp, fax._mfax_faxincomingarchive_getmessage, faxcomex/IFaxIncomingArchive::GetMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxIncomingArchive.GetMessage
 - IFaxIncomingArchive.GetMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingArchive::GetMessage


## -description


The <b>GetMessage</b> method returns a fax message from the archive of inbound faxes by using the fax message ID.


## -parameters




### -param bstrMessageId [in]

Type: <b>BSTR</b>

Specifies a null-terminated string that contains the message ID of the fax to retrieve from the archive of inbound faxes.


### -param pFaxIncomingMessage [out, retval]

Type: <b><a href="https://msdn.microsoft.com/29fa30c9-d4f2-4ed5-95fc-873f2263c7bb">IFaxIncomingMessage</a>**</b>

A <a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a> object.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_IN_ARCHIVE</a> access right. 




## -see-also




<a href="https://msdn.microsoft.com/a81d6314-b26f-4946-896e-218a0095938f">FaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/0442fc06-20b8-4608-8532-c8901832f39b">IFaxIncomingArchive</a>



<a href="https://msdn.microsoft.com/bdc7cdaa-0e37-4124-a9b3-9f9eabbe329e">Visual Basic Example</a>
 

 

