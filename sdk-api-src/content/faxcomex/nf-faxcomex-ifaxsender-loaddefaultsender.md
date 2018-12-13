---
UID: NF:faxcomex.IFaxSender.LoadDefaultSender
title: IFaxSender::LoadDefaultSender
author: windows-sdk-content
description: The IFaxSender::get_LoadDefaultSender method fills the FaxSender object with the default sender information.
old-location: fax\_mfax_faxsender_cpp_mfax_faxsender_loaddefaultsender_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_9ak2.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFaxSender interface [Fax Service],LoadDefaultSender method, IFaxSender.LoadDefaultSender, IFaxSender::LoadDefaultSender, LoadDefaultSender, LoadDefaultSender method [Fax Service], LoadDefaultSender method [Fax Service],IFaxSender interface, _mfax_faxsender.loaddefaultsender, fax._mfax_faxsender_cpp_mfax_faxsender_loaddefaultsender_cpp, fax._mfax_faxsender_loaddefaultsender, faxcomex/IFaxSender::LoadDefaultSender
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
 - IFaxSender.LoadDefaultSender
 - IFaxSender.LoadDefaultSender
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSender::LoadDefaultSender


## -description


The <b>IFaxSender::get_LoadDefaultSender</b> method fills the <a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a> object with the default sender information.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The default sender information is saved using the <a href="https://msdn.microsoft.com/en-us/library/ms689558(v=VS.85).aspx">IFaxSender::SaveDefaultSender</a> method.

This method can return remote procedure call (RPC) return values. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa378645(v=VS.85).aspx">RPC Return Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687533(v=VS.85).aspx">IFaxSender</a>



<a href="https://msdn.microsoft.com/en-us/library/ms693479(v=VS.85).aspx">Visual Basic Example</a>
 

 

