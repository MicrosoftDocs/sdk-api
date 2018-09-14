---
UID: NF:lmdfs.NetDfsSetInfo
title: NetDfsSetInfo function
author: windows-sdk-content
description: Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link target.
old-location: dfs\netdfssetinfo.htm
tech.root: Dfs
ms.assetid: 5526afa7-82bc-47c7-99d6-44e41ef772b1
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: 100, 101, 102, 103, 104, 105, 106, 107, 150, NetDfsSetInfo, NetDfsSetInfo function [Distributed File System], _win32_netdfssetinfo, dfs.netdfssetinfo, fs.netdfssetinfo, lmdfs/NetDfsSetInfo, netmgmt.netdfssetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmdfs.h
req.include-header: LmDfs.h, Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetDfsSetInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# NetDfsSetInfo function


## -description


Sets or modifies information about a specific Distributed File System (DFS) root, root target, link, or link 
    target.


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
       <i>link_path</i>  is a DFS link.

For a root, the string can be in one of two forms:

\\<i>ServerName</i>\<i>DfsName</i>

or

\\<i>DomainName</i>\<i>DomDfsname</i>

where the values of the names are the same as those described previously.


### -param ServerName [in, optional]

Pointer to a string that specifies the DFS link target server name. This parameter is optional. For more 
      information, see the Remarks section.


### -param ShareName [in, optional]

Pointer to a string that specifies the DFS link target share name. This may also be a share name with a 
      path relative to the share.  For example, "share1\mydir1\mydir2". This parameter is optional. For more 
      information, see the Remarks section.


### -param Level [in]

Specifies the information level of the data. This parameter can be one of the following values.



#### 100

Set the comment associated with the DFS root or link specified in the 
        <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
        <a href="https://msdn.microsoft.com/763ba0f0-01e9-47cf-bbe5-93e13aa83aa0">DFS_INFO_100</a> structure.



#### 101

Set the storage state associated with the DFS root or link specified in the 
        <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
        <a href="https://msdn.microsoft.com/506aaf68-2f23-4dd2-b43c-aeb86334a3d8">DFS_INFO_101</a> structure.



#### 102

Set the time-out value associated with the DFS root or link specified in the 
        <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
        <a href="https://msdn.microsoft.com/ca4da0a2-d5b3-4ad6-bc00-6629b9bf13e7">DFS_INFO_102</a> structure.



#### 103

Set the property flags for the DFS root or link specified in the <i>DfsEntryPath</i> 
         parameter. The <i>Buffer</i> parameter points to a 
         <a href="https://msdn.microsoft.com/d3d31087-770e-4434-8ee0-6183102a9a6b">DFS_INFO_103</a> structure.



#### 104

Set the target priority rank and class for the root target or link target specified in the 
         <i>DfsEntryPath</i> parameter. The <i>Buffer</i> parameter points to a 
         <a href="https://msdn.microsoft.com/95b2cd36-4933-440d-889d-ebf36d7b9cc7">DFS_INFO_104</a> structure.



#### 105

Set the comment, state, and time-out information, as well as property flags, for the DFS root or link 
         specified in the <i>DfsEntryPath</i> parameter. The <i>Buffer</i> 
         parameter points to a <a href="https://msdn.microsoft.com/b9ad9e41-d5b4-446f-ac99-a51808344f77">DFS_INFO_105</a> structure.



#### 106

Set the target state and priority for the root target or link target specified in the 
         <i>DfsEntryPath</i> parameter. This information cannot be set for a DFS namespace root or 
         link, only for a root target or link target. The <i>Buffer</i> parameter points to a 
         <a href="https://msdn.microsoft.com/12c114e4-f978-4423-85a8-ec0cf9c9e8c5">DFS_INFO_106</a> structure.



#### 107

Set the comment, state, time-out information, and property flags for the DFS root or link specified in the 
         <i>DfsEntryPath</i> parameter. For DFS links, you can also set the security descriptor for 
         the link's reparse point. The <i>Buffer</i> parameter points to a 
         <a href="https://msdn.microsoft.com/38afc682-bb37-42ad-9e92-a1b0aa277f29">DFS_INFO_107</a> structure.



#### 150

Set the security descriptor for a DFS link's reparse point. The <i>Buffer</i> parameter 
         points to a <a href="https://msdn.microsoft.com/b0fa6fca-8e60-447d-9334-c4df04f13439">DFS_INFO_150</a> structure.


### -param Buffer [in]

Pointer to a buffer that specifies the data. The format of this data depends on the value of the 
      <i>Level</i> parameter. For more information, see 
      <a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a>.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The caller must have Administrator privilege on the DFS server. For more information about calling functions 
    that require administrator privileges, see 
    <a href="https://msdn.microsoft.com/b25db548-d5ab-4276-9b50-36d030909384">Running with Special Privileges</a>.

If you specify both the <i>ServerName</i> and <i>ShareName</i> 
    parameters, the <b>NetDfsSetInfo</b> function sets or modifies information specific to 
    that root target or link target. If the parameters are <b>NULL</b>, the function sets or 
    modifies information that is specific to the DFS namespace root or the DFS link instead of a specific DFS root 
    target or link target.

Because only one comment and one time-out can be set for a DFS root or link, the 
    <i>ServerName</i> and <i>ShareName</i>  parameters are ignored for 
    information levels 100 and 102. These parameters are required for level 101.

For information level 101, the <b>DFS_VOLUME_STATE_RESYNCHRONIZE</b> and <b>DFS_VOLUME_STATE_STANDBY</b> state values can be 
     set as follows for a specific domain-based DFS root when there is more than one DFS root target for the DFS 
     namespace:

The <i>DfsEntryPath</i> parameter specifies the domain-based DFS namespace, and the 
      <i>ServerName</i> and <i>ShareName</i> parameters taken together specify 
      the DFS root target on which the set-information operation is to be performed.


#### Examples

The following code sample demonstrates how to associate a comment with a DFS link using a call to the 
     <b>NetDfsSetInfo</b> function. The sample specifies information level 100 
     (<a href="https://msdn.microsoft.com/763ba0f0-01e9-47cf-bbe5-93e13aa83aa0">DFS_INFO_100</a>).

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

void wmain(int argc, wchar_t *argv[])
{
   DFS_INFO_100 dfsData;
   DWORD res;
   //
   // Check command line arguments.
   //
   if (argc&lt;2)
      wprintf(L"Syntax: %s DfsEntryPath [\"Comment\"]\n", argv[0]);
   else
   {
      //
      // Fill in DFS_INFO_100 structure member.
      //
      dfsData.Comment = argc &lt; 3 ? NULL : argv[2];
      //
      // Call the NetDfsSetInfo function, specifying level 100.
      //
      res = NetDfsSetInfo(argv[1], NULL, NULL, 100, (LPBYTE) &amp;dfsData);
      //
      // Display the result of the call.
      //
      if(res == 0)
         printf("Comment set.\n");
      else
         printf("Error: %u", res);
   }
   return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/763ba0f0-01e9-47cf-bbe5-93e13aa83aa0">DFS_INFO_100</a>



<a href="https://msdn.microsoft.com/506aaf68-2f23-4dd2-b43c-aeb86334a3d8">DFS_INFO_101</a>



<a href="https://msdn.microsoft.com/ca4da0a2-d5b3-4ad6-bc00-6629b9bf13e7">DFS_INFO_102</a>



<a href="https://msdn.microsoft.com/d3d31087-770e-4434-8ee0-6183102a9a6b">DFS_INFO_103</a>



<a href="https://msdn.microsoft.com/95b2cd36-4933-440d-889d-ebf36d7b9cc7">DFS_INFO_104</a>



<a href="https://msdn.microsoft.com/b9ad9e41-d5b4-446f-ac99-a51808344f77">DFS_INFO_105</a>



<a href="https://msdn.microsoft.com/12c114e4-f978-4423-85a8-ec0cf9c9e8c5">DFS_INFO_106</a>



<a href="https://msdn.microsoft.com/38afc682-bb37-42ad-9e92-a1b0aa277f29">DFS_INFO_107</a>



<a href="https://msdn.microsoft.com/b0fa6fca-8e60-447d-9334-c4df04f13439">DFS_INFO_150</a>



<a href="https://msdn.microsoft.com/a29cde3e-483a-4658-94d4-27398f66abfb">Distributed File System (DFS) Functions</a>



<a href="https://msdn.microsoft.com/c05a8d78-41f4-4c19-a25e-ef4885869584">NetDfsEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management Overview</a>
 

 

