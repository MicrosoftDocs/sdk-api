---
UID: NF:faxcomex.IFaxIncomingMessage2.Save
title: IFaxIncomingMessage2::Save
author: windows-sdk-content
description: Saves the FaxIncomingMessage object's data.
old-location: fax\_mfax_faxincomingmessage2_cpp_mfax_faxincomingmessage_save_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\reference\serviceextendedcom\i\ifaxincomingmessage2\save.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
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


Saves the <a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a> object's data.


<div class="alert"><b>Note</b>  This method is supported only in Windows Vista and later.</div><div> </div>

## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To use this method, a user must have the <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2MANAGE_CONFIG</a> and <a href="https://msdn.microsoft.com/en-us/library/Aa359062(v=VS.85).aspx">far2QUERY_CONFIG</a> access rights.

It is not necessary to call this method to commit changes to the <a href="https://msdn.microsoft.com/en-us/library/Aa359006(v=VS.85).aspx">IFaxIncomingMessage2::Subject</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359005(v=VS.85).aspx">IFaxIncomingMessage2::SenderName</a>, <a href="https://msdn.microsoft.com/en-us/library/Aa359004(v=VS.85).aspx">IFaxIncomingMessage2::SenderFaxNumber</a>, and <a href="https://msdn.microsoft.com/en-us/library/Aa358996(v=VS.85).aspx">IFaxIncomingMessage2::HasCoverPage</a> properties. They are committed with the <a href="https://msdn.microsoft.com/en-us/library/Aa358998(v=VS.85).aspx">IFaxIncomingMessage2::Reassign</a> method.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms686126(v=VS.85).aspx">FaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/ms686128(v=VS.85).aspx">IFaxIncomingMessage</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa358995(v=VS.85).aspx">IFaxIncomingMessage2</a>
 

 

