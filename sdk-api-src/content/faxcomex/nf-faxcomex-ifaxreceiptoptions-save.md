---
UID: NF:faxcomex.IFaxReceiptOptions.Save
title: IFaxReceiptOptions::Save
author: windows-sdk-content
description: The IFaxReceiptOptions::Save method saves the FaxReceiptOptions object data.
old-location: fax\_mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_25ph.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxReceiptOptions interface [Fax Service],Save method, IFaxReceiptOptions.Save, IFaxReceiptOptions::Save, Save, Save method [Fax Service], Save method [Fax Service],IFaxReceiptOptions interface, _mfax_faxreceiptoptions.save, fax._mfax_faxreceiptoptions_cpp_mfax_faxreceiptoptions_save_cpp, fax._mfax_faxreceiptoptions_save, faxcomex/IFaxReceiptOptions::Save
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


The <b>IFaxReceiptOptions::Save</b> method saves the <a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a> object data.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is not supported for Windows XP when the receipt type is set to <a href="https://msdn.microsoft.com/en-us/library/ms688004(v=VS.85).aspx">frtMAIL</a>, or if <a href="https://msdn.microsoft.com/en-us/library/ms689610(v=VS.85).aspx">IFaxReceiptOptions::get_UseForInboundRouting </a> is set to <b>TRUE</b>. In these cases, this method will return the error: <a href="https://msdn.microsoft.com/en-us/library/ms693490(v=VS.85).aspx">FAX_E_NOT_SUPPORTED_ON_THIS_SKU</a>.

To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farMANAGE_CONFIG</a> and <a href="https://msdn.microsoft.com/en-us/library/ms689205(v=VS.85).aspx">farQUERY_CONFIG</a> access rights.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690118(v=VS.85).aspx">FaxReceiptOptions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690119(v=VS.85).aspx">IFaxReceiptOptions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693387(v=VS.85).aspx">Setting Receipt Options</a>
 

 

