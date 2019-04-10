---
UID: NF:faxcomex.IFaxSender.SaveDefaultSender
title: IFaxSender::SaveDefaultSender (faxcomex.h)
author: windows-sdk-content
description: The IFaxSender::SaveDefaultSender method stores information about the default sender from the FaxSender object.
old-location: fax\_mfax_faxsender_cpp_mfax_faxsender_savedefaultsender_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6uuq.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IFaxSender interface [Fax Service],SaveDefaultSender method, IFaxSender.SaveDefaultSender, IFaxSender::SaveDefaultSender, SaveDefaultSender, SaveDefaultSender method [Fax Service], SaveDefaultSender method [Fax Service],IFaxSender interface, _mfax_faxsender.savedefaultsender, fax._mfax_faxsender_cpp_mfax_faxsender_savedefaultsender_cpp, fax._mfax_faxsender_savedefaultsender, faxcomex/IFaxSender::SaveDefaultSender
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
 - IFaxSender.SaveDefaultSender
 - IFaxSender.SaveDefaultSender
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSender::SaveDefaultSender


## -description


The <b>IFaxSender::SaveDefaultSender</b> method stores information about the default sender from the <a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a> object.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To load the default sender information into a <a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a> object, use the <a href="https://msdn.microsoft.com/en-us/library/ms690195(v=VS.85).aspx">IFaxSender::get_LoadDefaultSender</a> method.

This method can return remote procedure call (RPC) return values. For more information, see <a href="https://msdn.microsoft.com/en-us/library/Aa378645(v=VS.85).aspx">RPC Return Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms687532(v=VS.85).aspx">FaxSender</a>



<a href="https://msdn.microsoft.com/en-us/library/ms687533(v=VS.85).aspx">IFaxSender</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692936(v=VS.85).aspx">Visual Basic Example</a>
 

 

