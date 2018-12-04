---
UID: NF:faxcomex.IFaxActivityLogging.get_LogIncoming
title: IFaxActivityLogging::get_LogIncoming
author: windows-sdk-content
description: The IFaxActivityLogging::get_LogIncoming property is a Boolean value that indicates whether the fax service logs entries for incoming faxes in the activity log database.
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logincoming_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3yef.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IFaxActivityLogging interface [Fax Service],LogIncoming property, IFaxActivityLogging.LogIncoming, IFaxActivityLogging.get_LogIncoming, IFaxActivityLogging.put_LogIncoming, IFaxActivityLogging::LogIncoming, IFaxActivityLogging::get_LogIncoming, IFaxActivityLogging::put_LogIncoming, LogIncoming property [Fax Service], LogIncoming property [Fax Service],IFaxActivityLogging interface, _mfax_faxactivitylogging.logincoming, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logincoming_cpp, fax._mfax_faxactivitylogging_logincoming, faxcomex/IFaxActivityLogging::LogIncoming, faxcomex/IFaxActivityLogging::get_LogIncoming, faxcomex/IFaxActivityLogging::put_LogIncoming, get_LogIncoming
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
 - IFaxActivityLogging.LogIncoming
 - IFaxActivityLogging.get_LogIncoming
 - IFaxActivityLogging.put_LogIncoming
 - IFaxActivityLogging.get_LogIncoming
 - IFaxActivityLogging.put_LogIncoming
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFaxActivityLogging::get_LogIncoming


## -description


The <b>IFaxActivityLogging::get_LogIncoming</b> property is a Boolean value that indicates whether the fax service logs entries for incoming faxes in the activity log database.

This property is read/write.


## -parameters


## -remarks



If this property is equal to <b>TRUE</b>, the fax service logs entries for incoming fax jobs in the activity log database. If this property is equal to <b>FALSE</b>, the fax service does not log entries.

To read or write to this property, a user must have the <a href="https://msdn.microsoft.com/70d729c6-8299-47d7-8dea-f7c754a25531">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://msdn.microsoft.com/225afdb8-7249-4aa5-bbde-638adf02eb41">FaxActivityLogging</a>



<a href="https://msdn.microsoft.com/77c3d94d-9076-4efd-833d-47373dc8b13b">IFaxActivityLogging</a>



<a href="https://msdn.microsoft.com/afee6ea0-f63d-4818-9ff0-1887638d232c">Visual Basic Example</a>
 

 

