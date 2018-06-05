---
UID: NF:faxcom.IFaxStatus.get_Receive
title: IFaxStatus::get_Receive
author: windows-sdk-content
description: Retrieves the Receive property for the FaxStatus object of a parent FaxPort object. The Receive property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.
old-location: fax\_mfax_ifaxstatus_get_receive_vb.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_5u1x.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: FaxStatus object [Fax Service],Receive property, FaxStatus.Receive, IFaxStatus.get_Receive, IFaxStatus::get_Receive, Receive property [Fax Service], Receive property [Fax Service],FaxStatus object, _mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_get_receive, fax._mfax_ifaxstatus_get_receive_vb, get_Receive
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Faxcom.dll
api_name:
-	FaxStatus.Receive
product: Windows
targetos: Windows
req.lib: 
req.dll: Faxcom.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFaxStatus::get_Receive


## -description


Retrieves the <b>Receive</b> property for the <a href="https://msdn.microsoft.com/88f02cb1-df32-4fb8-9fe7-6c3abe1948dc">FaxStatus</a> object of a parent <a href="https://msdn.microsoft.com/cc59452b-194e-4a68-955b-ac39cd5325ff">FaxPort</a> object. The <b>Receive</b> property is a Boolean value that indicates whether a specified fax port is currently receiving a fax.

This property is read-only.


## -parameters


## -remarks



To determine if a specified port is currently sending a fax, you can call the <a href="https://msdn.microsoft.com/e7759c8a-a6f3-4e42-9d56-bf93d11d7ad1">IFaxStatus::get_Send</a> method.




## -see-also




<a href="https://msdn.microsoft.com/f564dc20-7c7c-41c3-81a1-2dfc61ee09f1">Fax Service Client API Interfaces</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/ce382d4d-aeaf-4254-9bc7-74b7d1d7f1a4">FaxStatus</a>



<a href="https://msdn.microsoft.com/abdd91dd-7734-411a-9b7c-0da312269e6d">IFaxPort</a>



<a href="https://msdn.microsoft.com/e61b13b3-d86c-4f95-bf5a-6b0545a76d03">IFaxPorts</a>



<a href="https://msdn.microsoft.com/823cbedb-052a-4ac1-a73c-4bbafeac2523">IFaxStatus</a>



<a href="https://msdn.microsoft.com/e7759c8a-a6f3-4e42-9d56-bf93d11d7ad1">Send</a>
 

 

