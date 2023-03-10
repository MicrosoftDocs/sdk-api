---
UID: NF:faxcomex.IFaxActivityLogging.put_LogOutgoing
title: IFaxActivityLogging::put_LogOutgoing (faxcomex.h)
description: The IFaxActivityLogging::get_LogOutgoing property is a Boolean value that indicates whether the fax service logs entries for outgoing faxes in the activity log database. (Put)
helpviewer_keywords: ["IFaxActivityLogging interface [Fax Service]","LogOutgoing property","IFaxActivityLogging.LogOutgoing","IFaxActivityLogging.get_LogOutgoing","IFaxActivityLogging.put_LogOutgoing","IFaxActivityLogging::LogOutgoing","IFaxActivityLogging::get_LogOutgoing","IFaxActivityLogging::put_LogOutgoing","LogOutgoing property [Fax Service]","LogOutgoing property [Fax Service]","IFaxActivityLogging interface","_mfax_faxactivitylogging.logoutgoing","fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logoutgoing_cpp","fax._mfax_faxactivitylogging_logoutgoing","faxcomex/IFaxActivityLogging::LogOutgoing","faxcomex/IFaxActivityLogging::get_LogOutgoing","faxcomex/IFaxActivityLogging::put_LogOutgoing","put_LogOutgoing"]
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logoutgoing_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_5xt3.htm
ms.date: 12/05/2018
ms.keywords: IFaxActivityLogging interface [Fax Service],LogOutgoing property, IFaxActivityLogging.LogOutgoing, IFaxActivityLogging.get_LogOutgoing, IFaxActivityLogging.put_LogOutgoing, IFaxActivityLogging::LogOutgoing, IFaxActivityLogging::get_LogOutgoing, IFaxActivityLogging::put_LogOutgoing, LogOutgoing property [Fax Service], LogOutgoing property [Fax Service],IFaxActivityLogging interface, _mfax_faxactivitylogging.logoutgoing, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_logoutgoing_cpp, fax._mfax_faxactivitylogging_logoutgoing, faxcomex/IFaxActivityLogging::LogOutgoing, faxcomex/IFaxActivityLogging::get_LogOutgoing, faxcomex/IFaxActivityLogging::put_LogOutgoing, put_LogOutgoing
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
 - IFaxActivityLogging::put_LogOutgoing
 - faxcomex/IFaxActivityLogging::put_LogOutgoing
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
 - IFaxActivityLogging.LogOutgoing
 - IFaxActivityLogging.get_LogOutgoing
 - IFaxActivityLogging.put_LogOutgoing
 - IFaxActivityLogging.get_LogOutgoing
 - IFaxActivityLogging.put_LogOutgoing
---

# IFaxActivityLogging::put_LogOutgoing


## -description

The <b>IFaxActivityLogging::get_LogOutgoing</b> property is a Boolean value that indicates whether the fax service logs entries for outgoing faxes in the activity log database.

This property is read/write.

## -parameters

## -remarks

If this property is equal to <b>TRUE</b>, the fax service logs entries for outgoing fax jobs in the activity log database. If this property is equal to <b>FALSE</b>, the fax service does not log entries.

To read or write to this property, a user must have the <a href="/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivitylogging">IFaxActivityLogging</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-setting-logging-options">Visual Basic Example</a>
