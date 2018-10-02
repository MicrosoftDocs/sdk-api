---
UID: NF:faxcomex.IFaxIncomingMessage2.Save
title: IFaxIncomingMessage2::Save
author: windows-sdk-content
description: Saves the FaxIncomingMessage object's data.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\save.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IFaxIncomingMessage2 interface [Fax Service],Save method, IFaxIncomingMessage2.Save, IFaxIncomingMessage2::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxIncomingMessage2 interface, _mfax_faxincomingmessage.save, fax._mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_save_cpp, fax._mfax_faxincomingmessage_save, faxcomex/IFaxIncomingMessage2::Save
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IFaxIncomingMessage2.Save
 - IFaxIncomingMessage2.Save
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxIncomingMessage2::Save


## -description


Saves the <a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a> object's data.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2MANAGE_CONFIG</a> and <a href="https://msdn.microsoft.com/9765d6b3-7acd-4c20-8508-29fd28509fea">far2QUERY_CONFIG</a> access rights.

It is not necessary to call this method to commit changes to the <a href="https://msdn.microsoft.com/b6722c85-3750-4a5d-baf0-05c7f79c45af">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/dba0099d-bf47-47e0-8a83-39a2fe9f4793">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/304f722e-4ea6-472c-99c3-1b129d143dae">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://msdn.microsoft.com/71bd6223-e5d3-453c-b747-9b0be9b074c6">IFaxIncomingMessage2::HasCoverPage</a> properties. They are committed with the <a href="https://msdn.microsoft.com/befff3bc-4489-4a63-b231-ff2974c760d1">IFaxIncomingMessage2::Reassign</a> method.




## -see-also




<a href="https://msdn.microsoft.com/ee546d4c-e580-4738-a5d2-0b10c5d8a1ab">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/29fa30c9-d4f2-4ed5-95fc-873f2263c7bb">IFaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/b3dc429e-1470-4e7d-8cd5-9cadb0052051">IFaxIncomingMessage2</a>
 

 

