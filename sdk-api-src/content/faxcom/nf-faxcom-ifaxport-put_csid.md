---
UID: NF:faxcom.IFaxPort.put_Csid
title: IFaxPort::put_Csid (faxcom.h)
description: The IFaxPort::get_Csid property is a null-terminated string that contains the called station identifier (CSID) associated with the fax port. (Put)
helpviewer_keywords: ["Csid property [Fax Service]","Csid property [Fax Service]","IFaxPort interface","IFaxPort interface [Fax Service]","Csid property","IFaxPort.Csid","IFaxPort.put_Csid","IFaxPort::Csid","IFaxPort::get_Csid","IFaxPort::put_Csid","_mfax_ifaxport_get_csid","fax._mfax_ifaxport_get_csid","fax._mfax_ifaxport_mfax_ifaxport_get_csid_cpp","faxcom/IFaxPort::Csid","faxcom/IFaxPort::get_Csid","faxcom/IFaxPort::put_Csid","put_Csid"]
old-location: fax\_mfax_ifaxport_mfax_ifaxport_get_csid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_16ec.htm
ms.date: 12/05/2018
ms.keywords: Csid property [Fax Service], Csid property [Fax Service],IFaxPort interface, IFaxPort interface [Fax Service],Csid property, IFaxPort.Csid, IFaxPort.put_Csid, IFaxPort::Csid, IFaxPort::get_Csid, IFaxPort::put_Csid, _mfax_ifaxport_get_csid, fax._mfax_ifaxport_get_csid, fax._mfax_ifaxport_mfax_ifaxport_get_csid_cpp, faxcom/IFaxPort::Csid, faxcom/IFaxPort::get_Csid, faxcom/IFaxPort::put_Csid, put_Csid
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
 - IFaxPort::put_Csid
 - faxcom/IFaxPort::put_Csid
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
 - IFaxPort.Csid
 - IFaxPort.get_Csid
 - IFaxPort.put_Csid
---

# IFaxPort::put_Csid


## -description

The <b>IFaxPort::get_Csid</b> property is a null-terminated string that contains the called station identifier (CSID) associated with the fax port.  

This property is read/write.

## -parameters

## -remarks

<div class="alert"><b>Note</b>  Before setting a value for this property, a fax client application can call the <a href="/previous-versions/windows/desktop/fax/-mfax-ifaxport-get-canmodify-vb">IFaxPort::get_CanModify</a> property to ensure that the client has permission to modify configuration information for the specified fax port.</div>
<div> </div>
Only printable characters such as English letters, numeric symbols, and punctuation marks (ASCII range 0x20 to 0x7F) can be used in a CSID.

When the fax service receives a fax on a port, the service transmits the CSID to the sending device.

The T.30 specification of the International Telecommunication Union (ITU) restricts the value of a CSID to 20 ASCII characters. If a fax client application specifies a CSID that contains non-ASCII characters, the fax service removes them. If the CSID exceeds 20 characters, the service truncates the extra characters.

<b>IFaxPort::get_Csid</b> allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="/previous-versions/windows/desktop/api/oleauto/nf-oleauto-sysfreestring">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-freeing-fax-resources">Freeing Fax Resources</a>.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-interfaces">Fax Service Client API Interfaces</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxport">IFaxPort</a>



<a href="/previous-versions/windows/desktop/api/faxcom/nn-faxcom-ifaxports">IFaxPorts</a>
