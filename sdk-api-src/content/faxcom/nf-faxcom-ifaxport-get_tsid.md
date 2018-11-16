---
UID: NF:faxcom.IFaxPort.get_Tsid
title: IFaxPort::get_Tsid
author: windows-sdk-content
description: The IFaxPort::get_Tsid property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6p0k.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxPort interface [Fax Service],Tsid property, IFaxPort.Tsid, IFaxPort.get_Tsid, IFaxPort::Tsid, IFaxPort::get_Tsid, IFaxPort::put_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_tsid, fax._mfax_ifaxport_get_tsid, fax._mfax_ifaxport_mfax_ifaxport_get_tsid_cpp, faxcom/IFaxPort::Tsid, faxcom/IFaxPort::get_Tsid, faxcom/IFaxPort::put_Tsid, get_Tsid
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Faxcom.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - IFaxPort.Tsid
 - IFaxPort.get_Tsid
 - IFaxPort.put_Tsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- faxcom.h
: 
- IFaxPort.get_Tsid
: 
---

# IFaxPort::get_Tsid


## -description


The <b>IFaxPort::get_Tsid</b> property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/b09b6e5f-fa1d-4d0b-8581-e0ba779b72bb">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
Only printable characters such as English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) can be used in a called station identifier (CSID).

When the fax service receives a fax on a port, the service transmits the TSID to the receiving device.

The T.30 specification of the International Telecommunication Union (ITU) restricts the value of a TSID to 20 ASCII characters. If a fax client application specifies a TSID that contains non-ASCII characters, the fax service removes them. If the TSID exceeds 20 characters, the service truncates the extra characters.

<b>IFaxPort::get_Tsid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>
 

 

