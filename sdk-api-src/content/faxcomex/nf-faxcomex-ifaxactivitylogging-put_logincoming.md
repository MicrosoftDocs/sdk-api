---
UID: NF:faxcomex.IFaxActivityLogging.put_LogIncoming
title: IFaxActivityLogging::put_LogIncoming (faxcomex.h)
description: The IFaxActivityLogging::get_LogIncoming property is a Boolean value that indicates whether the fax service logs entries for incoming faxes in the activity log database. (Put)
helpviewer_keywords: ["IFaxActivityLogging interface [Fax Service]","LogIncoming property","IFaxActivityLogging.LogIncoming","IFaxActivityLogging.get_LogIncoming","IFaxActivityLogging.put_LogIncoming","IFaxActivityLogging::LogIncoming","IFaxActivityLogging::get_LogIncoming","IFaxActivityLogging::put_LogIncoming","LogIncoming property [Fax Service]","LogIncoming property [Fax Service]","IFaxActivityLogging interface","_mfax_faxactivitylogging.logincoming","fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logincoming_cpp","fax._mfax_faxactivitylogging_logincoming","faxcomex/IFaxActivityLogging::LogIncoming","faxcomex/IFaxActivityLogging::get_LogIncoming","faxcomex/IFaxActivityLogging::put_LogIncoming","put_LogIncoming"]
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logincoming_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_3yef.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivityLogging interface [Fax Service],LogIncoming property, IFaxActivityLogging.LogIncoming, IFaxActivityLogging.get_LogIncoming, IFaxActivityLogging.put_LogIncoming, IFaxActivityLogging::LogIncoming, IFaxActivityLogging::get_LogIncoming, IFaxActivityLogging::put_LogIncoming, LogIncoming property [Fax Service], LogIncoming property [Fax Service],IFaxActivityLogging interface, _mfax_faxactivitylogging.logincoming, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logincoming_cpp, fax._mfax_faxactivitylogging_logincoming, faxcomex/IFaxActivityLogging::LogIncoming, faxcomex/IFaxActivityLogging::get_LogIncoming, faxcomex/IFaxActivityLogging::put_LogIncoming, put_LogIncoming
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IFaxActivityLogging::put_LogIncoming
 - faxcomex/IFaxActivityLogging::put_LogIncoming
dev_langs:
 - c++
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
---

# IFaxActivityLogging::put_LogIncoming


## -description

The <b>IFaxActivityLogging::get_LogIncoming</b> property is a Boolean value that indicates whether the fax service logs entries for incoming faxes in the activity log database.

This property is read/write.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the fax service logs entries for incoming fax jobs in the activity log database. If this property is equal to <b>FALSE</b>, the fax service does not log entries.

To read or write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivitylogging">IFaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-logging-options">Visual Basic Example</a>
