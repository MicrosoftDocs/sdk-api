---
UID: NE:minwinbase._READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
title: READ_DIRECTORY_NOTIFY_INFORMATION_CLASS (minwinbase.h)
author: windows-sdk-content
description: Indicates the possible types of information that an application that calls the ReadDirectoryChangesExW function can request.
old-location: fs\read_directory_notify_information_class.htm
tech.root: FileIO
ms.assetid: 193D018B-80FE-45B2-826A-A00D173E32D3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS, PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS, PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration pointer [Files], READ_DIRECTORY_NOTIFY_INFORMATION_CLASS, READ_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration [Files], ReadDirectoryNotifyExtendedInformation, ReadDirectoryNotifyInformation, fs.read_directory_notify_information_class, minwinbase/PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS, minwinbase/READ_DIRECTORY_NOTIFY_INFORMATION_CLASS, minwinbase/ReadDirectoryNotifyExtendedInformation, minwinbase/ReadDirectoryNotifyInformation"
ms.topic: enum
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Minwinbase.h
api_name:
 - READ_DIRECTORY_NOTIFY_INFORMATION_CLASS
product: Windows
targetos: Windows
req.typenames: READ_DIRECTORY_NOTIFY_INFORMATION_CLASS, *PREAD_DIRECTORY_NOTIFY_INFORMATION_CLASS
req.redist: 
---

# READ_DIRECTORY_NOTIFY_INFORMATION_CLASS enumeration


## -description


Indicates the possible types of information that an application that calls the <a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a> function can request.


## -enum-fields




### -field ReadDirectoryNotifyInformation

The <a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a> function  should provide  information that describes the changes within the specified directory, and return this information in the  output buffer in the form of <a href="https://msdn.microsoft.com/cb95352f-8a15-48d8-9150-e4bc395e0122">FILE_NOTIFY_INFORMATION</a> structures.


### -field ReadDirectoryNotifyExtendedInformation

The <a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a> function  should provide  extended information that describes the changes within the specified directory, and return this information in the  output buffer in the form of <a href="https://msdn.microsoft.com/4558F2E8-F515-4202-9CAA-FDAF20160F61">FILE_NOTIFY_EXTENDED_INFORMATION</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/4558F2E8-F515-4202-9CAA-FDAF20160F61">FILE_NOTIFY_EXTENDED_INFORMATION</a>



<a href="https://msdn.microsoft.com/cb95352f-8a15-48d8-9150-e4bc395e0122">FILE_NOTIFY_INFORMATION</a>



<a href="https://msdn.microsoft.com/90C2F258-094C-4A0E-80E7-3FA241D288EA">ReadDirectoryChangesExW</a>
 

 

