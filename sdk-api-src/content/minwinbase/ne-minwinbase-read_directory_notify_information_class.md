---
UID: NE:minwinbase._READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
title: READ_DIRECTORY_NOTIFY_INFORMATION_CLASS (minwinbase.h)
description: Indicates the possible types of information that an application that calls the ReadDirectoryChangesExW function can request.
helpviewer_keywords: ["*PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS","PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS","PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration pointer [Files]","READ_DIRECTORY_NOTIFY_INFORMATION_CLASS","READ_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration [Files]","ReadDirectoryNotifyExtendedInformation","ReadDirectoryNotifyInformation","fs.read_directory_notify_information_class","minwinbase/PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS","minwinbase/READ_DIRECTORY_NOTIFY_INFORMATION_CLASS","minwinbase/ReadDirectoryNotifyExtendedInformation","minwinbase/ReadDirectoryNotifyInformation"]
old-location: fs\read_directory_notify_information_class.htm
tech.root: fs
ms.assetid: 193D018B-80FE-45B2-826A-A00D173E32D3
ms.date: 12/05/2018
ms.keywords: '*PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS, PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS, PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration pointer [Files], READ_DIRECTORY_NOTIFY_INFORMATION_CLASS, READ_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration [Files], ReadDirectoryNotifyExtendedInformation, ReadDirectoryNotifyInformation, fs.read_directory_notify_information_class, minwinbase/PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS, minwinbase/READ_DIRECTORY_NOTIFY_INFORMATION_CLASS, minwinbase/ReadDirectoryNotifyExtendedInformation, minwinbase/ReadDirectoryNotifyInformation'
req.header: minwinbase.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: READ_DIRECTORY_NOTIFY_INFORMATION_CLASS, *PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
 - minwinbase/_READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
 - PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS
 - minwinbase/PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS
 - READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
 - minwinbase/READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Minwinbase.h
api_name:
 - READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
---

# READ_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration


## -description

Indicates the possible types of information that an application that calls the <a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesexw">ReadDirectoryChangesExW</a> function can request.

## -enum-fields

### -field ReadDirectoryNotifyInformation:1

The <a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesexw">ReadDirectoryChangesExW</a> function  should provide  information that describes the changes within the specified directory, and return this information in the  output buffer in the form of <a href="/windows/desktop/api/winnt/ns-winnt-file_notify_information">FILE_NOTIFY_INFORMATION</a> structures.

### -field ReadDirectoryNotifyExtendedInformation

The <a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesexw">ReadDirectoryChangesExW</a> function  should provide  extended information that describes the changes within the specified directory, and return this information in the  output buffer in the form of <a href="/windows/desktop/api/winnt/ns-winnt-file_notify_extended_information">FILE_NOTIFY_EXTENDED_INFORMATION</a> structures.

## -see-also

<a href="/windows/desktop/api/winnt/ns-winnt-file_notify_extended_information">FILE_NOTIFY_EXTENDED_INFORMATION</a>



<a href="/windows/desktop/api/winnt/ns-winnt-file_notify_information">FILE_NOTIFY_INFORMATION</a>



<a href="/windows/desktop/api/winbase/nf-winbase-readdirectorychangesexw">ReadDirectoryChangesExW</a>
