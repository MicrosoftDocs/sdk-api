---
UID: NF:faxcom.IFaxStatus.get_Tsid
title: IFaxStatus::get_Tsid
author: windows-sdk-content
description: Retrieves the Tsid property for the FaxStatus object of a parent FaxPort object. The Tsid property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.
old-location: fax\_mfax_ifaxstatus_get_tsid_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_22p0.htm
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: FaxStatus object [Fax Service],Tsid property, FaxStatus.Tsid, IFaxStatus.get_Tsid, IFaxStatus::get_Tsid, Tsid property [Fax Service], Tsid property [Fax Service],FaxStatus object, _mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_get_tsid, fax._mfax_ifaxstatus_get_tsid_vb, get_Tsid
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
 - FaxStatus.Tsid
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_Tsid


## -description


Retrieves the <b>Tsid</b> property for the <a href="https://msdn.microsoft.com/library/ms691355(v=VS.85).aspx">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/library/ms691338(v=VS.85).aspx">FaxPort</a> object. The <b>Tsid</b> property is a null-terminated string that contains the transmitting station identifier (TSID) associated with the fax port.

This property is read-only.


## -parameters


## -remarks



The <b>Tsid</b> property is set for both inbound and outbound fax transmissions. If the TSID information is not available, the <b>IFaxStatus::get_Tsid</b> method returns an empty string.

The <b>IFaxStatus::get_Tsid</b> method allocates the memory required for the buffer pointed to by the pVal parameter. The client application must call the <a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a> function to deallocate the resources associated with this parameter. For more information, see <a href="https://msdn.microsoft.com/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms691931(v=VS.85).aspx">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms690310(v=VS.85).aspx">FaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms691281(v=VS.85).aspx">IFaxPort</a>



<a href="https://msdn.microsoft.com/library/ms690893(v=VS.85).aspx">IFaxPorts</a>



<a href="https://msdn.microsoft.com/library/ms690794(v=VS.85).aspx">IFaxStatus</a>



<a href="https://msdn.microsoft.com/library/ms221481(v=VS.85).aspx">SysFreeString</a>
 

 

