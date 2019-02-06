---
UID: NE:minwinbase._FINDEX_SEARCH_OPS
title: FINDEX_SEARCH_OPS
author: windows-sdk-content
description: Defines values that are used with the FindFirstFileEx function to specify the type of filtering to perform.
old-location: fs\findex_search_ops_str.htm
tech.root: FileIO
ms.assetid: 3f4c18fb-e128-421f-bd05-456d4d3698a7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: FINDEX_SEARCH_OPS, FINDEX_SEARCH_OPS enumeration [Files], FindExSearchLimitToDevices, FindExSearchLimitToDirectories, FindExSearchNameMatch, _win32_findex_search_ops_str, base.findex_search_ops_str, fs.findex_search_ops_str, winbase/FINDEX_SEARCH_OPS, winbase/FindExSearchLimitToDevices, winbase/FindExSearchLimitToDirectories, winbase/FindExSearchNameMatch
ms.topic: enum
req.header: minwinbase.h
req.include-header: Minwinbase.h, Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
 - WinBase.h
api_name:
 - FINDEX_SEARCH_OPS
product: Windows
targetos: Windows
req.typenames: FINDEX_SEARCH_OPS
req.redist: 
---

# FINDEX_SEARCH_OPS enumeration


## -description


Defines values that are used with the 
    <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function to specify the type of 
    filtering to perform.


## -enum-fields




### -field FindExSearchNameMatch

The search for a file that matches a specified file name.
      

The <i>lpSearchFilter</i> parameter of 
       <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> must be 
       <b>NULL</b> when this search operation is used.


### -field FindExSearchLimitToDirectories

This is an advisory flag. 
If the file system supports directory filtering, the function searches for a file that matches the specified  name and is also a directory.
If the file system does not support directory filtering, this flag is silently ignored.


The <i>lpSearchFilter</i> parameter of the <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function must be <b>NULL</b> when this search value is used.

If directory filtering is desired, this flag can be used on all file systems, but because it is  an advisory flag and  only affects file systems that support it, the application must examine the file attribute data stored in the <i>lpFindFileData</i> parameter of the <a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a> function to determine whether the function has  returned a handle to a directory.


### -field FindExSearchLimitToDevices

This filtering type is not available.
      

For more information, see 
       <a href="Http://go.microsoft.com/fwlink/p/?linkid=94247">Device Interface Classes</a>.


### -field FindExSearchMaxSearchOp




## -see-also




<a href="https://msdn.microsoft.com/9f40e98f-153f-4b65-afd9-06742684c100">FindFirstFileEx</a>
 

 

