---
UID: NF:faxcomex.IFaxSender.SaveDefaultSender
title: IFaxSender::SaveDefaultSender
author: windows-sdk-content
description: The IFaxSender::SaveDefaultSender method stores information about the default sender from the FaxSender object.
old-location: fax\_mfax_faxsender_cpp_mfax_faxsender_savedefaultsender_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinto_z_6uuq.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: IFaxSender interface [Fax Service],SaveDefaultSender method, IFaxSender.SaveDefaultSender, IFaxSender::SaveDefaultSender, SaveDefaultSender, SaveDefaultSender method [Fax Service], SaveDefaultSender method [Fax Service],IFaxSender interface, _mfax_faxsender.savedefaultsender, fax._mfax_faxsender_cpp_mfax_faxsender_savedefaultsender_cpp, fax._mfax_faxsender_savedefaultsender, faxcomex/IFaxSender::SaveDefaultSender
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
 - IFaxSender.SaveDefaultSender
 - IFaxSender.SaveDefaultSender
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxSender::SaveDefaultSender


## -description


The <b>IFaxSender::SaveDefaultSender</b> method stores information about the default sender from the <a href="https://msdn.microsoft.com/f265cfd0-cf62-4d86-9ba5-d1842ac94baa">FaxSender</a> object.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



To load the default sender information into a <a href="https://msdn.microsoft.com/f265cfd0-cf62-4d86-9ba5-d1842ac94baa">FaxSender</a> object, use the <a href="https://msdn.microsoft.com/c41343c0-2d97-4bc5-ba22-a7dfec5cb336">IFaxSender::get_LoadDefaultSender</a> method.

This method can return remote procedure call (RPC) return values. For more information, see <a href="_rpc_rpc_return_values">RPC Return Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/f265cfd0-cf62-4d86-9ba5-d1842ac94baa">FaxSender</a>



<a href="https://msdn.microsoft.com/c22bd4df-6ce2-4491-91c9-7bb8c8f7eafd">IFaxSender</a>



<a href="https://msdn.microsoft.com/347943cc-a417-469e-a936-8da5601e752f">Visual Basic Example</a>
 

 

