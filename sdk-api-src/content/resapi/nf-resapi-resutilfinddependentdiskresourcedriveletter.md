---
UID: NF:resapi.ResUtilFindDependentDiskResourceDriveLetter
title: ResUtilFindDependentDiskResourceDriveLetter function (resapi.h)
description: Retrieves the drive letter associated with a Physical Disk dependency of a resource. The PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER type defines a pointer to this function.
helpviewer_keywords: ["PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER","PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER function [Failover Cluster]","ResUtilFindDependentDiskResourceDriveLetter","ResUtilFindDependentDiskResourceDriveLetter function [Failover Cluster]","_wolf_resutilfinddependentdiskresourcedriveletter","mscs.resutilfinddependentdiskresourcedriveletter","resapi/PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER","resapi/ResUtilFindDependentDiskResourceDriveLetter"]
old-location: mscs\resutilfinddependentdiskresourcedriveletter.htm
tech.root: MsCS
ms.assetid: 8f2187e3-6bb7-4756-af2b-a28857581bcb
ms.date: 12/05/2018
ms.keywords: PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER, PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER function [Failover Cluster], ResUtilFindDependentDiskResourceDriveLetter, ResUtilFindDependentDiskResourceDriveLetter function [Failover Cluster], _wolf_resutilfinddependentdiskresourcedriveletter, mscs.resutilfinddependentdiskresourcedriveletter, resapi/PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER, resapi/ResUtilFindDependentDiskResourceDriveLetter
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
req.lib: ResUtils.lib
req.dll: ResUtils.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ResUtilFindDependentDiskResourceDriveLetter
 - resapi/ResUtilFindDependentDiskResourceDriveLetter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - ResUtils.dll
api_name:
 - ResUtilFindDependentDiskResourceDriveLetter
---

# ResUtilFindDependentDiskResourceDriveLetter function


## -description

Retrieves the drive letter associated with a 
    <a href="/previous-versions/windows/desktop/mscs/physical-disk">Physical Disk</a>
<a href="/previous-versions/windows/desktop/mscs/resource-dependencies">dependency</a> of a 
    <a href="/previous-versions/windows/desktop/mscs/resources">resource</a>. The <b>PRESUTIL_FIND_DEPENDENT_DISK_RESOURCE_DRIVE_LETTER</b> type defines a pointer to this function.

## -parameters

### -param hCluster [in]

Cluster handle.

### -param hResource [in]

Handle to the resource to query for dependencies.

### -param pszDriveLetter [out]

Buffer in which to store the drive letter.

### -param pcchDriveLetter [in, out]

On input, specifies the size of the <i>pszDriveLetter</i> buffer as a count of 
       <b>WCHAR</b>s. On output, specifies the size of the resulting data as a count of 
       <b>WCHAR</b>s that includes the terminating <b>NULL</b>.

## -returns

If the operations succeeds, the function returns <b>ERROR_SUCCESS</b> (0).

If the operation fails, the function returns a 
       <a href="/windows/desktop/Debug/system-error-codes">system error code</a>. The following are possible error 
       codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NO_MORE_ITEMS</b></dt>
</dl>
</td>
<td width="60%">
No Physical Disk dependency was found in the specified resource's list of dependencies.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_RESOURCE_NOT_PRESENT</b></dt>
</dl>
</td>
<td width="60%">
No drive letter could be returned.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
The buffer passed in was too small. The <i>pcchDriveLetter</i> parameter specifies the 
         required size.

</td>
</tr>
</table>

## -remarks

Do not call this function from a <a href="/previous-versions/windows/desktop/mscs/resource-dlls">resource DLL</a>. It will 
     cause a deadlock. You should have your resource extension call this function and write the results out as a 
     private property that your resource DLL can then read.

If the resource identified by hResource depends on more than one Physical Disk resource, 
     <b>ResUtilFindDependentDiskResourceDriveLetter</b> 
     returns the drive letter of the first Physical Disk dependency that is enumerated for the resource.


#### Examples

The following example takes a resource name as a command line argument and displays the drive letter 
      associated with the resource's Physical Disk dependency (if any). This example uses the 
      <a href="/previous-versions/windows/desktop/mscs/clusdocex-h">ClusDocEx.h</a> header file defined in the Failover Cluster 
      documentation.


```cpp
//////////////////////////////////////////////////////////////////////

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
                                                          &cchResDrive );

        if( dw == ERROR_MORE_DATA )
         {
          delete [] pszResDrive;
          pszResDrive = new WCHAR[cchResDrive];
          dw = ResUtilFindDependentDiskResourceDriveLetter( hCluster,
                                                            hRes,
                                                            pszResDrive,
                                                            &cchResDrive );
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

```


If the resource identified by <i>hResource</i> refers to a mount point disk, there may or 
      may not be a drive letter associated with the disk resource. If the mount point disk has no associated drive 
      letter, the value returned by 
      <b>ResUtilFindDependentDiskResourceDriveLetter</b> 
      will be in the format of <i>DiskXPartitionY</i>, which is valid data but cannot be passed 
      directly to file system APIs such as <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>.

The following example takes the output string from 
      <b>ResUtilFindDependentDiskResourceDriveLetter</b> 
      and transforms it to Win32 format. The output string from this function can be passed to 
      <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>. If the function fails, the return value is 
      <b>NULL</b>; call <a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> to 
      get extended error info. If the function succeeds the user has to free the buffer returned using 
      <a href="/windows/desktop/api/winbase/nf-winbase-localfree">LocalFree</a>.


```cpp
#define UNICODE 1
#define _UNICODE 1
#pragma comment(lib, "ResUtils.lib")

#include <windows.h>
#include <stdlib.h>
#include <ResApi.h>
#include <strsafe.h>

#define IS_DRIVELETTER(x) ((iswalpha((x)[0])) && ((x)[1] == L':'))
#define IS_NTPATH(x) ((wcsstr((x), L"Disk") != NULL) && (wcsstr((x), L"Partition") != NULL)) 
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
    swscanf_s(InputString, L"Disk%uPartition%u", &diskNum, &partNum);
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

```

## -see-also

<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependency">ResUtilGetResourceDependency</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyclass">ResUtilGetResourceDependencyByClass</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependencybyname">ResUtilGetResourceDependencyByName</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcedependentipaddressprops">ResUtilGetResourceDependentIPAddressProps</a>



<a href="/windows/desktop/api/resapi/nf-resapi-resutilgetresourcenamedependency">ResUtilGetResourceNameDependency</a>



<a href="/previous-versions/windows/desktop/mscs/resource-utility-functions">Resource Utility Functions</a>