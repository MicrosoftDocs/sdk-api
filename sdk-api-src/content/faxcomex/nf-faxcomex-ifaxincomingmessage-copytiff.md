---
UID: NF:faxcomex.IFaxIncomingMessage.CopyTiff
title: IFaxIncomingMessage::CopyTiff
author: windows-sdk-content
description: The CopyTiff method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.
old-location: fax\_mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_copytiff_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_1vc6.htm
ms.author: windowssdkdev
ms.date: 10/09/2018
ms.keywords: CopyTiff, CopyTiff method [Fax Service], CopyTiff method [Fax Service],IFaxIncomingMessage interface, IFaxIncomingMessage interface [Fax Service],CopyTiff method, IFaxIncomingMessage.CopyTiff, IFaxIncomingMessage::CopyTiff, _mfax_faxincomingmessage.copytiff, fax._mfax_faxincomingmessage_copytiff, fax._mfax_faxincomingmessage_cpp_mfax_faxincomingmessage_copytiff_cpp, faxcomex/IFaxIncomingMessage::CopyTiff
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
 - IFaxIncomingMessage.CopyTiff
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage::CopyTiff


## -description


The <b>CopyTiff</b> method copies the Tagged Image File Format Class F (TIFF Class F) file associated with the inbound fax message to a file on the local computer.


## -parameters




### -param bstrTiffPath [in]

Type: <b>BSTR</b>

Null-terminated <b>BSTR</b> that specifies a fully qualified path and file name on the local computer. The fax service will copy the TIFF Class F file associated with the inbound fax message to the specified file.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/29fa30c9-d4f2-4ed5-95fc-873f2263c7bb">IFaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/1e66b30d-e74f-4c73-b005-acd2d0fd8893">Visual Basic Example</a>
 

 

