---
UID: NF:faxcom.IFaxDoc.get_Tsid
title: IFaxDoc::get_Tsid
author: windows-sdk-content
description: Sets or retrieves the Tsid property of a FaxDoc object. The Tsid property is a null-terminated string that contains a user-defined transmitting station identifier (TSID).
old-location: fax\_mfax_ifaxdoc_mfax_ifaxdoc_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_3xyc.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxDoc interface [Fax Service],Tsid property, IFaxDoc.Tsid, IFaxDoc.get_Tsid, IFaxDoc::Tsid, IFaxDoc::get_Tsid, IFaxDoc::put_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxDoc interface, _mfax_ifaxdoc_get_tsid, fax._mfax_ifaxdoc_get_tsid, fax._mfax_ifaxdoc_mfax_ifaxdoc_get_tsid_cpp, faxcom/IFaxDoc::Tsid, faxcom/IFaxDoc::get_Tsid, faxcom/IFaxDoc::put_Tsid, get_Tsid
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
 - IFaxDoc.Tsid
 - IFaxDoc.get_Tsid
 - IFaxDoc.put_Tsid
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
- IFaxDoc.get_Tsid
: 
---

# IFaxDoc::get_Tsid


## -description


Sets or retrieves the <b>Tsid</b> property of a <a href="https://msdn.microsoft.com/11462af9-20c2-4661-801e-dcc3e092283d">FaxDoc</a> object. The <b>Tsid</b> property is a null-terminated string that contains a user-defined transmitting station identifier (TSID).

This property is read/write.


## -parameters


## -remarks



If the fax server allows user-defined TSID strings, the service will transmit the value of the <i>pVal</i> parameter to the receiving fax device instead of the TSID associated with the sending device. You can call the <a href="https://msdn.microsoft.com/a27d55e8-68c0-4700-becb-d56ecddbef44">UseDeviceTsid</a> method to determine whether the fax server is configured to permit user-specified TSIDs.

If the fax server allows user-defined TSID strings, the service will transmit the value of <i>pVal</i> to the receiving fax device instead of the TSID associated with the sending device. You can use the <a href="https://msdn.microsoft.com/a27d55e8-68c0-4700-becb-d56ecddbef44">UseDeviceTsid</a> property to determine whether the fax server is configured to permit user-specified TSIDs.

The TSID is typically the fax number of the device sending the transmission. Note that the T.30 specification of the International Telecommunication Union (ITU) restricts the value of a TSID to 20 ASCII characters. If a fax client application specifies a TSID that contains non-ASCII characters, the fax service removes them. If the TSID exceeds 20 characters, the service truncates the extra characters.

The <b>get_Tsid</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/16f68004-fa4d-40c7-90a5-0bb562e72bd7">IFaxDoc</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>



<a href="https://msdn.microsoft.com/a27d55e8-68c0-4700-becb-d56ecddbef44">UseDeviceTsid</a>
 

 

