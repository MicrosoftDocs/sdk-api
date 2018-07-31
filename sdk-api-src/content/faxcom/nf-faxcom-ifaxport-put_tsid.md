---
UID: NF:faxcom.IFaxPort.put_Tsid
title: IFaxPort::put_Tsid
author: windows-sdk-content
description: The Tsid property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.
old-location: fax\_mfax_ifaxport_get_tsid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6p0k.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxPort object [Fax Service],Tsid property, FaxPort.Tsid, IFaxPort.put_Tsid, IFaxPort::put_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],FaxPort object, _mfax_ifaxport_get_tsid, fax._mfax_ifaxport_get_tsid, fax._mfax_ifaxport_get_tsid_vb, put_Tsid
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: ShellWindowTypeConstants
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Faxcom.dll
api_name:
 - FaxPort.Tsid
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::put_Tsid


## -description


The <b>Tsid</b> property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms692798(v=VS.85).aspx">CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
Only printable characters such as English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) can be used in a called station identifier (CSID).

When the fax service receives a fax on a port, the service transmits the TSID to the receiving device.

The T.30 specification of the International Telecommunication Union (ITU) restricts the value of a TSID to 20 ASCII characters. If a fax client application specifies a TSID that contains non-ASCII characters, the fax service removes them. If the TSID exceeds 20 characters, the service truncates the extra characters.

<b>Tsid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690315(v=VS.85).aspx">FaxPort</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>
 

 

