---
UID: NF:faxcom.IFaxStatus.get_Tsid
title: IFaxStatus::get_Tsid
author: windows-sdk-content
description: Retrieves the Tsid property for the FaxStatus object of a parent FaxPort object. The Tsid property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_tsid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_22p0.htm
ms.author: windowssdkdev
ms.date: 11/08/2018
ms.keywords: IFaxStatus interface [Fax Service],Tsid property, IFaxStatus.Tsid, IFaxStatus.get_Tsid, IFaxStatus::Tsid, IFaxStatus::get_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],IFaxStatus interface, _mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_tsid_cpp, faxcom/IFaxStatus::Tsid, faxcom/IFaxStatus::get_Tsid, get_Tsid
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
 - IFaxStatus.Tsid
 - IFaxStatus.get_Tsid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_Tsid


## -description


Retrieves the <b>Tsid</b> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Tsid</b> property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.

This property is read-only.


## -parameters


## -remarks



The <b>Tsid</b> property is set for both inbound and outbound fax transmissions. If the TSID information is not available, the <b>IFaxStatus::get_Tsid</b> method returns an empty string.

The <b>IFaxStatus::get_Tsid</b> method allocates the memory required for the buffer pointed to by the pVal parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

