---
UID: NC:resapi.PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER
title: PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER
author: windows-driver-content
description: Retrieves the drive letter associated with a Physical Disk dependency of a resource. The PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER type defines a pointer to this function.
old-location: mscs\resutilfinddependentdiskresourcedriveletter.htm
old-project: MsCS
ms.assetid: 8f2187e3-6bb7-4756-af2b-a28857581bcb
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER, PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER callback function [Failover Cluster], _wolf_resutilfinddependentdiskresourcedriveletter, mscs.resutilfinddependentdiskresourcedriveletter, resapi/PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: callback
req.header: resapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RENDEZVOUS_SESSION_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	UserDefined
api_location:
-	ResApi.h
api_name:
-	PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER callback


## -description


Retrieves the drive letter associated with a 
    <a href="https://msdn.microsoft.com/d42e9bca-3717-44f7-a1b9-dfad1dbddd23">Physical Disk</a>
<a href="https://msdn.microsoft.com/2ad913d2-99cb-4885-a1de-822f77dc2030">dependency</a> of a 
    <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resource</a>. The <b>PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER</b> type defines a pointer to this function.


## -parameters




### -param hCluster [in]

Cluster handle.


### -param hResource [in]

Handle to the resource to query for dependencies.


### -param pszDriveLetter [out]

Buffer in which to store the drive letter.


### -param *pcchDriveLetter [in, out]

On input, specifies the size of the <i>pszDriveLetter</i> buffer as a count of 
       <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
       <b>WCHAR</b>s that includes the terminating <b>NULL</b>.


## -returns



If the operations succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error code</a>. The following are possible error 
       codes.




## -remarks



Do not call this function from a <a href="https://msdn.microsoft.com/e1434102-afaf-4a35-887e-a434c628bd90">resource DLL</a>. It will 
     cause a deadlock. You should have your resource extension call this function and write the results out as a 
     private property that your resource DLL can then read.

If the resource identified by hResource depends on more than one Physical Disk resource, 
     <i>ResUtilFindDependentDiskResourceDriveLetter</i> 
     returns the drive letter of the first Physical Disk dependency that is enumerated for the resource.


#### Examples

The following example takes a resource name as a command line argument and displays the drive letter 
      associated with the resource's Physical Disk dependency (if any). This example uses the 
      <a href="https://msdn.microsoft.com/fc2032d2-40a5-45bd-8661-1e778789bad6">ClusDocEx.h</a> header file defined in the Failover Cluster 
      documentation.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>//////////////////////////////////////////////////////////////////////

#include "ClusDocEx.h"

int main( int argc, char argv[] )
 {
  HCLUSTER  hCluster     = NULL;
  HRESOURCE hRes         = NULL;
  DWORD     dw;
  DWORD     cchResDrive  = ClusDocEx_DEFAULT_CCH;
  DWORD     cchResName   = ClusDocEx_DEFAULT_CCH;
  WCHAR     *pszResDrive = new WCHAR[cchResDrive];
  WCHAR     *pszResName  = new WCHAR[cchResName];

  dw = ClusDocEx_ConvertArg( argv[1], pszResName, cchResName );

  if( dw == ERROR_SUCCESS )
   {
    hCluster = ClusDocEx_OpenLocalClusterWithName();
    if( hCluster != NULL )
     {
      hRes = OpenClusterResource( hCluster, pszResName );
      if( hRes != NULL )
       {
        dw = ResUtilFindDependentDiskResourceDriveLetter( hCluster,
                                                          hRes,
                                                          pszResDrive,
                                                          &amp;cchResDrive );

        if( dw == ERROR_MORE_DATA )
         {
          delete [] pszResDrive;
          pszResDrive = new WCHAR[cchResDrive];
          dw = ResUtilFindDependentDiskResourceDriveLetter( hCluster,
                                                            hRes,
                                                            pszResDrive,
                                                            &amp;cchResDrive );
         }

        switch( dw )
         {
          case ERROR_SUCCESS:    
            wprintf( L"%ls depends on drive %ls.\n", pszResName, pszResDrive );
            break;

          case ERROR_NO_MORE_ITEMS:
          case ERROR_RESOURCE_NOT_PRESENT:
            wprintf( L"No Physical Disk dependency found for %ls.\n", pszResName );
            break;

          default:    
            ClusDocEx_DebugPrint( L"Could not obtain drive information", dw );
            break;
         }
        CloseClusterResource( hRes );
       }
      else // if hRes == NULL
       {
        ClusDocEx_DebugPrint( L"Could not open a resource handle", GetLastError() );
       }
      CloseCluster( hCluster );
     }
    else // if hCluster == NULL
     {
      ClusDocEx_DebugPrint( L"Could not open a cluster handle", GetLastError() );
     }

   }
  delete [] pszResName;
  delete [] pszResDrive;
  return 0;
 }
</pre>
</td>
</tr>
</table></span></div>
If the resource identified by <i>hResource</i> refers to a mount point disk, there may or 
      may not be a drive letter associated with the disk resource. If the mount point disk has no associated drive 
      letter, the value returned by 
      <i>ResUtilFindDependentDiskResourceDriveLetter</i> 
      will be in the format of <i>DiskXPartitionY</i>, which is valid data but cannot be passed 
      directly to file system APIs such as <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>.

The following example takes the output string from 
      <i>ResUtilFindDependentDiskResourceDriveLetter</i> 
      and transforms it to Win32 format. The output string from this function can be passed to 
      <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>. If the function fails, the return value is 
      <b>NULL</b>; call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to 
      get extended error info. If the function succeeds the user has to free the buffer returned using 
      <a href="https://msdn.microsoft.com/a0393983-cb43-4dfa-91a6-d82a5fb8de12">LocalFree</a>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#define UNICODE 1
#define _UNICODE 1
#pragma comment(lib, "ResUtils.lib")

#include &lt;windows.h&gt;
#include &lt;stdlib.h&gt;
#include &lt;ResApi.h&gt;
#include &lt;strsafe.h&gt;

#define IS_DRIVELETTER(x) ((iswalpha((x)[0])) &amp;&amp; ((x)[1] == L':'))
#define IS_NTPATH(x) ((wcsstr((x), L"Disk") != NULL) &amp;&amp; (wcsstr((x), L"Partition") != NULL)) 
#define GLOBALROOT_DISK_FORMAT L"\\\\\?\\GLOBALROOT\\Device\\Harddisk%u\\Partition%u"

LPWSTR ConvertNtDiskPathToW32DiskPath( LPCWSTR InputString )
 {
  LPWSTR outputString=NULL;
  DWORD status=ERROR_INVALID_PARAMETER;
  DWORD len;
  DWORD diskNum, partNum;

  if ((InputString == NULL) || (InputString[0] == 0))
   {
    goto Error_exit;
   }

  // Find out the required buffer size.
  len = 0;
  if (IS_DRIVELETTER(InputString))
   {
    len = wcslen(InputString) + 4;
   }
  else if (IS_NTPATH(InputString))
   {
    len = wcslen(GLOBALROOT_DISK_FORMAT) + 16;
   }
  else
   {
    //Malformed string.
    goto Error_exit;
   } 

  if ((outputString = (LPWSTR)LocalAlloc(LPTR, len * sizeof(WCHAR))) == NULL)
   {
    status = GetLastError();
    goto Error_exit;
   }

  if (IS_DRIVELETTER(InputString))
   {
    StringCchCopyW(outputString, len, InputString);
   }
  else
   {
    //Has to be NT path format.
    swscanf_s(InputString, L"Disk%uPartition%u", &amp;diskNum, &amp;partNum);
    StringCchPrintfW(outputString, len, GLOBALROOT_DISK_FORMAT, diskNum, partNum);
   }
    
  status = ERROR_SUCCESS;
    
Error_exit: 

  if (status != ERROR_SUCCESS)
   {
    if (outputString)
     {
      LocalFree(outputString);
     }
    SetLastError(status);
    return NULL;
   }

  return outputString;
 }
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/eee267b4-4272-4938-b061-02990ec528f2">ResUtilGetResourceDependency</a>



<a href="https://msdn.microsoft.com/7c2bd24a-8034-4a5f-8218-0a23d5e29b07">ResUtilGetResourceDependencyByClass</a>



<a href="https://msdn.microsoft.com/8c978b27-fd1a-47b6-8a30-cfe6e4fbcf57">ResUtilGetResourceDependencyByName</a>



<a href="https://msdn.microsoft.com/283b0086-1dbf-45dc-9651-93af9a9ff6d0">ResUtilGetResourceDependentIPAddressProps</a>



<a href="https://msdn.microsoft.com/071f11bb-fcb3-4c76-ad81-b19ff7bdcb4a">ResUtilGetResourceNameDependency</a>



<a href="https://msdn.microsoft.com/42eb7c1b-6bd6-4997-b33e-ed16470c8475">Resource Utility Functions</a>
 

 

