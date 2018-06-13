---
UID: NF:faxcom.IFaxPort.GetStatus
title: IFaxPort::GetStatus
author: windows-sdk-content
description: The GetStatus method creates a FaxStatus object for the parent FaxPort object. The FaxStatus object contains the current status of a fax port.
old-location: fax\_mfax_ifaxport_getstatus_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_8lo3.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FaxPort object [Fax Service],GetStatus method, FaxPort.GetStatus, GetStatus, GetStatus method [Fax Service], GetStatus method [Fax Service],FaxPort object, IFaxPort.GetStatus, IFaxPort::GetStatus, _mfax_ifaxport_getstatus, fax._mfax_ifaxport_getstatus, fax._mfax_ifaxport_getstatus_vb
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
 - FaxPort.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxPort::GetStatus


## -description


The <b>GetStatus</b> method creates a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object for the parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The FaxStatus object contains the current status of a fax port.


## -parameters




### -param retval






#### - retVal [out]

Type: <b><a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>*</b>

Retrieves a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object.


## -remarks



The <b>GetStatus</b> method retrieves an <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface pointer to a <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object. A fax client application can also access the <a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a> interface directly by calling the <a href="_com_IUnknown_QueryInterface">IUnknown::QueryInterface</a> method to retrieve an <b>IFaxStatus</b> interface pointer.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/7888d042-7d85-4921-b233-f6e95e0c80d9">FaxPort</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a>
 

 

