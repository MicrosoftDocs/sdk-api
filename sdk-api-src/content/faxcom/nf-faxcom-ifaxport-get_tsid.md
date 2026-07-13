---
UID: NF:faxcom.IFaxPort.get_Tsid
title: IFaxPort::get_Tsid (faxcom.h)
description: The IFaxPort::get_Tsid property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port. (Get)
helpviewer_keywords: ["IFaxPort interface [Fax Service]","Tsid property","IFaxPort.Tsid","IFaxPort.get_Tsid","IFaxPort::Tsid","IFaxPort::get_Tsid","IFaxPort::put_Tsid","Tsid property [Fax Service]","Tsid property [Fax Service]","IFaxPort interface","_mfax_ifaxport_get_tsid","fax._mfax_ifaxport_get_tsid","fax._mfax_ifaxport_mfax_ifaxport_get_tsid_cpp","faxcom/IFaxPort::Tsid","faxcom/IFaxPort::get_Tsid","faxcom/IFaxPort::put_Tsid","get_Tsid"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6p0k.htm
ms.date: 12/05/2018
ms.keywords: IFaxPort interface [Fax Service],Tsid property, IFaxPort.Tsid, IFaxPort.get_Tsid, IFaxPort::Tsid, IFaxPort::get_Tsid, IFaxPort::put_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxPort interface, _mfax_ifaxport_get_tsid, fax._mfax_ifaxport_get_tsid, fax._mfax_ifaxport_mfax_ifaxport_get_tsid_cpp, faxcom/IFaxPort::Tsid, faxcom/IFaxPort::get_Tsid, faxcom/IFaxPort::put_Tsid, get_Tsid
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxPort::get_Tsid
 - faxcom/IFaxPort::get_Tsid
dev_langs:
 - c++
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
---

# IFaxPort::get_Tsid


## -description

The <b>IFaxPort::get_Tsid</b> property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-canmodify-vb">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
Only printable characters such as English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) can be used in a called station identifier (CSID).

When the fax service receives a fax on a port, the service transmits the TSID to the receiving device.

The T.30 specification of the International Telecommunication Union (ITU) restricts the value of a TSID to 20 ASCII characters. If a fax client application specifies a TSID that contains non-ASCII characters, the fax service removes them. If the TSID exceeds 20 characters, the service truncates the extra characters.

<b>IFaxPort::get_Tsid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>
