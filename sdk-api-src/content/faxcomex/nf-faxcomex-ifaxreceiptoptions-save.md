---
UID: NF:faxcomex.IFaxReceiptOptions.Save
title: IFaxReceiptOptions::Save
author: windows-sdk-content
description: The IFaxReceiptOptions::Save method saves the FaxReceiptOptions object data.
old-location: fax\_mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_25ph.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxReceiptOptions interface [Fax Service],Save method, IFaxReceiptOptions.Save, IFaxReceiptOptions::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxReceiptOptions interface, _mfax_faxreceiptoptions.save, fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_save_cpp, fax._mfax_faxreceiptoptions_save, faxcomex/IFaxReceiptOptions::Save
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
 - IFaxReceiptOptions.Save
 - IFaxReceiptOptions.Save
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxReceiptOptions::Save


## -description


The <b>IFaxReceiptOptions::Save</b> method saves the <a href="https://msdn.microsoft.com/6c3d1358-6819-42e3-9be0-896ed7e2d463">FaxReceiptOptions</a> object data.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is not supported for Windows XP when the receipt type is set to <a href="https://msdn.microsoft.com/d334b8e4-bc4f-4f1f-9268-65a2106d3fa6">frtMAIL</a>, or if <a href="https://msdn.microsoft.com/ac1a3bde-d729-4669-b7e1-40bd6a00f921">IFaxReceiptOptions::get_UseForInboundRouting </a> is set to <b>TRUE</b>. In these cases, this method will return the error: <a href="https://msdn.microsoft.com/b5d59fec-2802-40bd-8ce4-748137f30fb2">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farMANAGE_CONFIG</a> and <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/6c3d1358-6819-42e3-9be0-896ed7e2d463">FaxReceiptOptions</a>



<a href="https://msdn.microsoft.com/95bcade2-eb0c-4e6f-8f3b-9d001f999992">IFaxReceiptOptions</a>



<a href="https://msdn.microsoft.com/4558e770-c6ae-4892-a2b3-40c59f6275fa">Setting Receipt Options</a>
 

 

