---
UID: NF:faxcomex.IFaxActivityLogging.get_DatabasePath
title: IFaxActivityLogging::get_DatabasePath (faxcomex.h)
author: windows-sdk-content
description: The IFaxActivityLogging::get_DatabasePath property is a null-terminated string that contains the path to the activity log database file.
old-location: fax\_mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_databasepath_cpp.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxinta_n_93vs.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DatabasePath property [Fax Service], DatabasePath property [Fax Service],IFaxActivityLogging interface, IFaxActivityLogging interface [Fax Service],DatabasePath property, IFaxActivityLogging.DatabasePath, IFaxActivityLogging.get_DatabasePath, IFaxActivityLogging.put_DatabasePath, IFaxActivityLogging::DatabasePath, IFaxActivityLogging::get_DatabasePath, IFaxActivityLogging::put_DatabasePath, _mfax_faxactivitylogging.databasepath, fax._mfax_faxactivitylogging_cpp_mfax_faxactivitylogging_databasepath_cpp, fax._mfax_faxactivitylogging_databasepath, faxcomex/IFaxActivityLogging::DatabasePath, faxcomex/IFaxActivityLogging::get_DatabasePath, faxcomex/IFaxActivityLogging::put_DatabasePath, get_DatabasePath
ms.topic: method
f1_keywords: 
 - "faxcomex/IFaxActivityLogging.DatabasePath"
dev_langs:
 - c++
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
 - IFaxActivityLogging.DatabasePath
 - IFaxActivityLogging.get_DatabasePath
 - IFaxActivityLogging.put_DatabasePath
 - IFaxActivityLogging.get_DatabasePath
 - IFaxActivityLogging.put_DatabasePath
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IFaxActivityLogging::get_DatabasePath


## -description


The <b>IFaxActivityLogging::get_DatabasePath</b> property is a null-terminated string that contains the path to the activity log database file.

This property is read/write.


## -parameters


## -remarks



<div class="alert"><b>Note</b>  If you change the path to the activity log directory, be sure to use a secured directory.</div>
<div> </div>
To read or write to this property, a user must have the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/ne-faxcomex-fax_access_rights_enum">farQUERY_CONFIG</a> access right.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/fax/-mfax-faxactivitylogging">FaxActivityLogging</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/faxcomex/nn-faxcomex-ifaxactivitylogging">IFaxActivityLogging</a>
 

 

