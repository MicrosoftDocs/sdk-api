---
UID: NF:wincon.SetConsoleTitleW
title: SetConsoleTitleW function
author: windows-driver-content
description: Sets the title for the current console window.
old-location: consoles\setconsoletitle.htm
old-project: consoles
ms.assetid: f1db449b-0dd0-4d61-bb79-b7da9a5168f4
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: SetConsoleTitle, SetConsoleTitle function [Consoles], SetConsoleTitleA, SetConsoleTitleW, _win32_setconsoletitle, base.setconsoletitle, consoles.setconsoletitle, wincon/SetConsoleTitle, wincon/SetConsoleTitleA, wincon/SetConsoleTitleW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SetConsoleTitleW (Unicode) and SetConsoleTitleA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: WICMetadataPattern
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
-	API-MS-Win-Core-Console-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	SetConsoleTitle
-	SetConsoleTitleA
-	SetConsoleTitleW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# SetConsoleTitleW function


## -description


Sets the title for the current console window.


## -parameters




### -param lpConsoleTitle [in]

The string to be displayed in the title bar of the console window. The total size must be less than 64K.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



When the process terminates, the system restores the original console title.

This function uses either Unicode characters or 8-bit characters from the console's current code page. The console's code page defaults initially to the system's OEM code page. To change the console's code page, use the 
<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a> or 
<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a> functions, or use the <b>chcp</b> or <b>mode con cp select=</b> commands.


#### Examples

The following example shows how to retrieve and modify the console title.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#include &lt;windows.h&gt;
#include &lt;tchar.h&gt;
#include &lt;conio.h&gt;
#include &lt;strsafe.h&gt;

int main( void )
{
   TCHAR szOldTitle[MAX_PATH];
   TCHAR szNewTitle[MAX_PATH];

   // Save current console title.

   if( GetConsoleTitle(szOldTitle, MAX_PATH) )
   {
      // Build new console title string.

      StringCchPrintf(szNewTitle, MAX_PATH, TEXT("TEST: %s"), szOldTitle);

      // Set console title to new title
      if( !SetConsoleTitle(szNewTitle) )
      {
         _tprintf(TEXT("SetConsoleTitle failed (%d)\n"), GetLastError());
         return 1;
      }
      else
      {
         _tprintf(TEXT("SetConsoleTitle succeeded.\n"));
      }
   }
   return 0;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/e3dd02f4-4899-4df0-a960-3b2625c15fee">GetConsoleOriginalTitle</a>



<a href="https://msdn.microsoft.com/c58bba36-9813-4bdc-83bf-30d55f8d7d79">GetConsoleTitle</a>



<a href="https://msdn.microsoft.com/6a1a9ba5-c792-491d-ae51-979f462dcb53">SetConsoleCP</a>



<a href="https://msdn.microsoft.com/0b41e66b-ca19-4d69-9f39-92da158344ef">SetConsoleOutputCP</a>
 

 

