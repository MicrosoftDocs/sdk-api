---
UID: NF:vdmdbg.VDMEnumProcessWOW
title: VDMEnumProcessWOW function
author: windows-sdk-content
description: Enumerates all virtual DOS machines running 16-bit Windows tasks.
old-location: winprog\vdmenumprocesswow.htm
tech.root: devnotes
ms.assetid: fd79ff50-cac2-40e0-86ad-2d6af97c99a9
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: VDMEnumProcessWOW, VDMEnumProcessWOW function [Windows API], vdmdbg/VDMEnumProcessWOW, winprog.vdmenumprocesswow
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: vdmdbg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: VdmDbg.lib
req.dll: VdmDbg.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - VdmDbg.dll
api_name:
 - VDMEnumProcessWOW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- VDMEnumProcessWOW
: 
---

# VDMEnumProcessWOW function


## -description


<p class="CCE_Message">[This function is not supported and may be altered or unavailable in the future.]

Enumerates all virtual DOS machines running 16-bit Windows tasks.


## -parameters




### -param fp [in]

A pointer to a callback function. The function is called for each enumerated VDM. For details, see the <a href="https://msdn.microsoft.com/ba5ce19d-4f37-4764-9a76-0f1013f9ea0f">ProcessVDMs</a> callback function.


### -param lparam [in]

A user-defined value that is passed to the callback function.


## -returns



The number of VDMs running, or the number enumerated before enumeration was terminated.




## -remarks



These VDMs contain the WowExec.exe task. DOS VDMs are not enumerated. To enumerate DOS VDMs, you need to use another method. First, you could use VDMEnumProcessWOW() to make a list of all Win16 VDMs, and then enumerate all instances of NTVDM.exe using some other scheme (such as PSAPI). Any NTVDM.exe from the full enumeration that was not in the Win16 list is a DOS VDM.


#### Examples

The following example shows how to enumerate virtual DOS machines running 16-bit Windows tasks.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>   // Enumerate all 16-bit tasks on the system.
   
   #include &lt;windows.h&gt;
   #include &lt;stdio.h&gt;
   #include &lt;vdmdbg.h&gt;

   BOOL WINAPI ProcessVDMs( DWORD, DWORD, LPARAM );
   BOOL WINAPI ProcessTasks( DWORD, WORD, WORD, PSZ, PSZ, LPARAM );

   #pragma comment( lib, "vdmdbg.lib" )
   
   void main()
   {
      // Enumerate VDMs
      VDMEnumProcessWOW(
         (PROCESSENUMPROC)ProcessVDMs,
         (LPARAM)NULL
      );

   }

   BOOL WINAPI ProcessVDMs( DWORD dwProcessId, DWORD dwAttrib,
      LPARAM t )
   {
      printf("\nProcess ID: %d\n", dwProcessId);

      // Use process ID of VDM to enumerate through its tasks
      VDMEnumTaskWOWEx(
         dwProcessId,
         (TASKENUMPROCEX)ProcessTasks,
         (LPARAM)NULL
      );

      // Keep enumerating
      return FALSE;
   }

   BOOL WINAPI ProcessTasks( DWORD dwThreadId, WORD hMod16, WORD hTask16,
      PSZ pszModName, PSZ pszFileName, LPARAM lParam )
   {
      // Print task's information
      printf("Thread ID: %d\n", dwThreadId);
      printf("Module handle: %d\n", hMod16);
      printf("Task handle: %d\n", hTask16);
      printf("Module Name: %s\n", pszModName);
      printf("File Name: %s\n", pszFileName);

      // Keep enumerating
      return FALSE;
   }

</pre>
</td>
</tr>
</table></span></div>


