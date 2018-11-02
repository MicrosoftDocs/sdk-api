---
UID: NF:faxcomex.IFaxActivityLogging.put_LogOutgoing
title: IFaxActivityLogging::put_LogOutgoing
author: windows-sdk-content
description: The IFaxActivityLogging::get_LogOutgoing property is a Boolean value that indicates whether the fax service logs entries for outgoing faxes in the activity log database.
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logoutgoing_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5xt3.htm
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IFaxActivityLogging interface [Fax Service],LogOutgoing property, IFaxActivityLogging.LogOutgoing, IFaxActivityLogging.get_LogOutgoing, IFaxActivityLogging.put_LogOutgoing, IFaxActivityLogging::LogOutgoing, IFaxActivityLogging::get_LogOutgoing, IFaxActivityLogging::put_LogOutgoing, LogOutgoing property [Fax Service], LogOutgoing property [Fax Service],IFaxActivityLogging interface, _mfax_faxactivitylogging.logoutgoing, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logoutgoing_cpp, fax._mfax_faxactivitylogging_logoutgoing, faxcomex/IFaxActivityLogging::LogOutgoing, faxcomex/IFaxActivityLogging::get_LogOutgoing, faxcomex/IFaxActivityLogging::put_LogOutgoing, put_LogOutgoing
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: faxcomex.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
req.dll: Fxscomex.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fxscomex.dll
api_name:
 - IFaxActivityLogging.LogOutgoing
 - IFaxActivityLogging.get_LogOutgoing
 - IFaxActivityLogging.put_LogOutgoing
 - IFaxActivityLogging.get_LogOutgoing
 - IFaxActivityLogging.put_LogOutgoing
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxActivityLogging::put_LogOutgoing


## -description


The <b>IFaxActivityLogging::get_LogOutgoing</b> property is a Boolean value that indicates whether the fax service logs entries for outgoing faxes in the activity log database.

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, the fax service logs entries for outgoing fax jobs in the activity log database. If this property is equal to <b>FALSE</b>, the fax service does not log entries.

To read or write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/225afdb8-7249-4aa5-bbde-638adf02eb41">FaxActivityLogging</a>



<a href="https://msdn.microsoft.com/77c3d94d-9076-4efd-833d-47373dc8b13b">IFaxActivityLogging</a>



<a href="https://msdn.microsoft.com/afee6ea0-f63d-4818-9ff0-1887638d232c">Visual Basic Example</a>
 

 

