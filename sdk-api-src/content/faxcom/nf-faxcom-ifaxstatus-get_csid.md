---
UID: NF:faxcom.IFaxStatus.get_Csid
title: IFaxStatus::get_Csid
author: windows-sdk-content
description: Retrieves the Csid property for the FaxStatus object of a parent FaxPort object. The Csid property is a string that contains called station identifier (CSID) information, typically the fax number of the receiving device.
old-location: fax\_mfax_ifaxstatus_mfax_ifaxstatus_get_csid_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_6k2s.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: Csid property [Fax Service], Csid property [Fax Service],IFaxStatus interface, IFaxStatus interface [Fax Service],Csid property, IFaxStatus.Csid, IFaxStatus.get_Csid, IFaxStatus::Csid, IFaxStatus::get_Csid, _mfax_ifaxstatus_get_csid, fax._mfax_ifaxstatus_get_csid, fax._mfax_ifaxstatus_mfax_ifaxstatus_get_csid_cpp, faxcom/IFaxStatus::Csid, faxcom/IFaxStatus::get_Csid, get_Csid
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
 - IFaxStatus.Csid
 - IFaxStatus.get_Csid
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxStatus::get_Csid


## -description


Retrieves the <b>Csid</b> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Csid</b> property is a string that contains called station identifier (CSID) information, typically the fax number of the receiving device.

This property is read-only.


## -parameters


## -remarks



If the CSID information is not available, the <b>IFaxStatus::get_Csid</b> method returns an empty string.

The <b>IFaxStatus::get_Csid</b> method allocates the memory required for the buffer pointed to by the <i>pVal</i> parameter. The client application must call the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

