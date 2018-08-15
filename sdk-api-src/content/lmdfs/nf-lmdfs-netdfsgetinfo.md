---
UID: NF:lmdfs.NetDfsGetInfo
title: NetDfsGetInfo function
author: windows-sdk-content
description: Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.
old-location: dfs\netdfsgetinfo.htm
old-project: dfs
ms.assetid: bbb2f24d-1c49-4016-a16b-60fde4a78193
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: 1, 100, 150, 2, 3, 4, 5, 50, 6, 7, 8, 9, NetDfsGetInfo, NetDfsGetInfo function [Distributed File System], _win32_netdfsgetinfo, dfs.netdfsgetinfo, fs.netdfsgetinfo, lmdfs/NetDfsGetInfo, netmgmt.netdfsgetinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: DFS_TARGET_PRIORITY_CLASS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsGetInfo
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetDfsGetInfo function


## -description


Retrieves information about a specified Distributed File System (DFS) root or link in a DFS namespace.


## -parameters




### -param DfsEntryPath [in]

Pointer to a string that specifies the Universal Naming Convention (UNC) path of a DFS root or link.

For a link, the string can be in one of two forms. The first form is as follows:

\\<i>ServerName</i>\<i>DfsName</i>\<i>link_path</i>

where <i>ServerName</i> is the name of the root target server that hosts the stand-alone 
       DFS namespace; <i>DfsName</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

The second form is as follows:

\\<i>DomainName</i>\<i>DomDfsname</i>\<i>link_path</i>

where <i>DomainName</i> is the name of the domain that hosts the domain-based DFS 
       namespace; <i>DomDfsname</i> is the name of the DFS namespace; and 
       <i>link_path</i> is a DFS link.

For a root, the string can be in one of two forms:

\\<i>ServerName</i>\<i>DfsName</i>

or

\\<i>DomainName</i>\<i>DomDfsname</i>

where the values of the names are the same as those described previously.

This parameter is required.


### -param ServerName [in, optional]

This parameter is currently ignored and should be <b>NULL</b>.


### -param ShareName [in, optional]

This parameter is currently ignored and should be <b>NULL</b>.


### -param Level [in]

Specifies the information level of the request. This parameter can be one of the following values.



#### 1

Return the DFS root or DFS link name. The <i>Buffer</i> parameter points to a 
        <a href="https://msdn.microsoft.com/96647570-badd-4925-ab90-054a00ba04c4">DFS_INFO_1</a> structure.



#### 2

Return the DFS root or DFS link name, status, and the number of DFS targets. The 
        <i>Buffer</i> parameter points to a 
        <a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a> structure.



#### 3

Return the DFS root or DFS link name, status, and  target information. The 
        <i>Buffer</i> parameter points to a 
        <a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a> structure.



#### 4

Return the DFS root or DFS link name, status, GUID, time-out, and target information. The 
        <i>Buffer</i> parameter points to a 
        <a href="https://msdn.microsoft.com/0b255be8-b719-4f40-9051-7e8a1bffa0e0">DFS_INFO_4</a> structure.



#### 5

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, and number of targets for a DFS 
         root and all links under the root. The <i>Buffer</i> parameter points to an array of 
         <a href="https://msdn.microsoft.com/bd68d7bf-94e1-41f9-84e9-e58ab34378a1">DFS_INFO_5</a> structures.



#### 6

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, DFS target information for a root 
         or link, and a list of DFS targets. The <i>Buffer</i> parameter points to an array of 
         <a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a> structures.



#### 7

Return the version number <b>GUID</b> of the DFS metadata. The <i>Buffer</i> parameter points 
         to an array of <a href="https://msdn.microsoft.com/03bcd93d-e3ec-49aa-be6c-399922f67c28">DFS_INFO_7</a> structures.



#### 8

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, number of targets, and link reparse 
         point security descriptors for a DFS root and all links under the root. The <i>Buffer</i> 
         parameter points to an array of <a href="https://msdn.microsoft.com/d1f1051e-fe4d-4771-9665-85d6f718b081">DFS_INFO_8</a> structures.



#### 9

Return the name, status, <b>GUID</b>, time-out, property flags, metadata size, DFS target information, link 
         reparse point security descriptors, and a list of DFS targets for a root or link. The 
         <i>Buffer</i> parameter points to an array of 
         <a href="https://msdn.microsoft.com/d09ebaa7-4ec7-4d25-8b77-fe568264e6b9">DFS_INFO_9</a> structures.



#### 50

Return the DFS metadata version and capabilities of an existing DFS namespace. The 
         <i>Buffer</i> parameter points to a 
         <a href="https://msdn.microsoft.com/1af2866c-fe83-43fc-b4cc-9976157fb269">DFS_INFO_50</a> structure.



#### 100

Return a comment about the DFS root or DFS link. The <i>Buffer</i> parameter points to 
        a <a href="https://msdn.microsoft.com/763ba0f0-01e9-47cf-bbe5-93e13aa83aa0">DFS_INFO_100</a> structure.



#### 150

Return the security descriptor for the DFS link's reparse point. The <i>Buffer</i> 
         parameter points to a <a href="https://msdn.microsoft.com/b0fa6fca-8e60-447d-9334-c4df04f13439">DFS_INFO_150</a> structure.

<div class="alert"><b>Note</b>  This value is natively supported only if the DFS link resides on a server that is running 
         Windows Server 2008 or later.</div>
<div> </div>

### -param Buffer [out]

Pointer to the address of a buffer that receives the requested information structures. The format of this 
      data depends on the value of the <i>Level</i> parameter. This buffer is allocated by the 
      system and must be freed using the 
      <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. For more information, 
      see 
      <a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> 
      and 
      <a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


## -returns



If the function succeeds, the return value is <b>NERR_Success</b>.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



No special group membership is required for using the 
    <b>NetDfsGetInfo</b> function.

An application calling the <b>NetDfsGetInfo</b> function may 
    indirectly cause the local DFS Namespace server servicing the function call to perform a full synchronization of 
    the related namespace metadata from the PDC emulator master for that domain. This full synchronization could 
    happen even when root scalability mode is configured for that namespace. In order to avoid this side-effect, if 
    the intent is to only retrieve the physical UNC pathname used by a specific DFSN client machine corresponding a 
    given DFS namespace path, then one alternative is to use the WDK API 
    <a href="https://msdn.microsoft.com/007df07e-685b-4224-b9d6-55e87cf0bd5c">ZwQueryInformationFile</a>, passing 
    <b>FileNetworkPhysicalNameInformation</b> as the 
    <i>FileInformationClass</i> parameter and passing the address of a caller-allocated 
    <a href="https://msdn.microsoft.com/04F6A7B1-1198-4E5F-B6A8-70EEABE7CE83">FILE_NETWORK_PHYSICAL_NAME_INFORMATION</a> 
    structure as the <i>FileInformation</i> parameter. Please see the WDK for more information on 
    calling WDK APIs.


#### Examples

The following code sample demonstrates how to retrieve information about a DFS link using a call to the 
     <b>NetDfsGetInfo</b> function. The sample calls 
     <b>NetDfsGetInfo</b>, specifying information level 3 
     (<a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a>). If the call succeeds, the 
     sample prints information about the DFS link, including the name and status of each target referenced by the 
     link. Finally, the code sample frees the memory allocated for the information buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;lm.h&gt;
#include &lt;lmdfs.h&gt;
#include &lt;stdio.h&gt;
#pragma comment(lib, "Netapi32.lib")

void wmain(int argc, wchar_t *argv[ ])
{
   PDFS_INFO_3 pData;
   PDFS_STORAGE_INFO ps;
   DWORD er = 0, tr = 0, res, j;

   //
   // Check command line arguments.
   //
   if (argc&lt;2)
      wprintf(L"Syntax: %s DfsEntryPath\n", argv[0]);
   else
   {
      //
      // Call the NetDfsGetInfo function, specifying level 3.
      //
      res = NetDfsGetInfo(argv[1], NULL, NULL, 3, (LPBYTE *) &amp;pData);
      //
      // If the call succeeds, print the data.
      //
      if(res==0)
      {
         printf("%-30S Storages: %u\nComment: %S\n", pData-&gt;EntryPath, pData-&gt;NumberOfStorages, pData-&gt;Comment);
         ps = pData-&gt;Storage;
         //
         // Loop through each target.
         //
         for(j = 1; j &lt;= pData-&gt;NumberOfStorages;j++)
         {
            //
            // Print the status (Offline/Online) and the name 
            // of each target referenced by the DFS link.
            //
            printf("    %S  ", (ps-&gt;State == DFS_STORAGE_STATE_OFFLINE) ? TEXT("Offline"): TEXT("Online "));
            printf("\\\\%S\\%S\n", ps-&gt;ServerName, ps-&gt;ShareName);
            ps++;
         }
         //
         // Free the allocated memory.
         //
         NetApiBufferFree(pData);
      }
      else
         printf("Error: %u\n", res);
   }
   return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/96647570-badd-4925-ab90-054a00ba04c4">DFS_INFO_1</a>



<a href="https://msdn.microsoft.com/763ba0f0-01e9-47cf-bbe5-93e13aa83aa0">DFS_INFO_100</a>



<a href="https://msdn.microsoft.com/c5fe27be-fd6e-4cf0-abf6-8363c78edf5b">DFS_INFO_2</a>



<a href="https://msdn.microsoft.com/fd60cb52-fa17-4cac-a7e8-9803303336dc">DFS_INFO_3</a>



<a href="https://msdn.microsoft.com/0b255be8-b719-4f40-9051-7e8a1bffa0e0">DFS_INFO_4</a>



<a href="https://msdn.microsoft.com/bd68d7bf-94e1-41f9-84e9-e58ab34378a1">DFS_INFO_5</a>



<a href="https://msdn.microsoft.com/96a9c5eb-f79f-4577-b320-ebacff84fcc4">DFS_INFO_6</a>



<a href="https://msdn.microsoft.com/03bcd93d-e3ec-49aa-be6c-399922f67c28">DFS_INFO_7</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>
 

 

