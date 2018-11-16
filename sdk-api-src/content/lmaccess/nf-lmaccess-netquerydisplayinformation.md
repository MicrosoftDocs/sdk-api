---
UID: NF:lmaccess.NetQueryDisplayInformation
title: NetQueryDisplayInformation function
author: windows-sdk-content
description: The NetQueryDisplayInformation function returns user account, computer, or group account information. Call this function to quickly enumerate account information for display in user interfaces.
old-location: netmgmt\netquerydisplayinformation.htm
tech.root: NetMgmt
ms.assetid: 049f1ea3-4d23-4b35-8b08-7256859aed45
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: 1, 2, 3, NetQueryDisplayInformation, NetQueryDisplayInformation function [Network Management], _win32_netquerydisplayinformation, lmaccess/NetQueryDisplayInformation, netmgmt.netquerydisplayinformation
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: lmaccess.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - NetQueryDisplayInformation
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- NetQueryDisplayInformation
: 
---

# NetQueryDisplayInformation function


## -description


The 
				<b>NetQueryDisplayInformation</b> function returns user account, computer, or group account information. Call this function to quickly enumerate account information for display in user interfaces.


## -parameters




### -param ServerName [in]

Pointer to a constant string that specifies the DNS or NetBIOS name of the remote server on which the function is to execute. If this parameter is <b>NULL</b>, the local computer is used.


### -param Level [in]

Specifies the information level of the data. This parameter can be one of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="1"></a><dl>
<dt><b>1</b></dt>
</dl>
</td>
<td width="60%">
Return user account information. The <i>SortedBuffer</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/308966f7-448c-4748-bbe7-9ac63afae1d9">NET_DISPLAY_USER</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return individual computer information. The <i>SortedBuffer</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/bdb1bef0-51f1-41d7-97fb-bda4ad24e386">NET_DISPLAY_MACHINE</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return group account information. The <i>SortedBuffer</i> parameter points to an array of 
<a href="https://msdn.microsoft.com/8e467f20-2cfb-40ae-a8b2-a5350d736eed">NET_DISPLAY_GROUP</a> structures.

</td>
</tr>
</table>
 


### -param Index [in]

Specifies the index of the first entry for which to retrieve information. Specify zero to retrieve account information beginning with the first display information entry. For more information, see the following Remarks section.


### -param EntriesRequested [in]

Specifies the maximum number of entries for which to retrieve information. On Windows 2000 and later, each call to 
<b>NetQueryDisplayInformation</b> returns a maximum of 100 objects.


### -param PreferredMaximumLength [in]

Specifies the preferred maximum size, in bytes, of the system-allocated buffer returned in the <i>SortedBuffer</i> parameter. It is recommended that you set this parameter to MAX_PREFERRED_LENGTH.


### -param ReturnedEntryCount [out]

Pointer to a value that receives the number of entries in the buffer returned in the <i>SortedBuffer</i> parameter. If this parameter is zero, there are no entries with an index as large as that specified. Entries may be returned when the function's return value is either NERR_Success or ERROR_MORE_DATA.


### -param SortedBuffer [out]

Pointer to a buffer that receives a pointer to a system-allocated buffer that specifies a sorted list of the requested information. The format of this data depends on the value of the <i>Level</i> parameter. Because this buffer is allocated by the system, it must be freed using the 
<a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA. For more information, see the following Return Values section, and the topics 
<a href="https://msdn.microsoft.com/f27e6cf5-f26a-4e6c-8d77-873bff6cc8e4">Network Management Function Buffers</a> and 
<a href="https://msdn.microsoft.com/08599966-68a1-420b-bbc7-6daac833d08f">Network Management Function Buffer Lengths</a>.


## -returns



If the function succeeds, the return value is NERR_Success.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
The user does not have access to the requested information.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_LEVEL</b></dt>
</dl>
</td>
<td width="60%">
The <i>Level</i> parameter specifies an invalid value.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_MORE_DATA</b></dt>
</dl>
</td>
<td width="60%">
More entries are available. That is, the last entry returned in the <i>SortedBuffer</i> parameter is not the last entry available. To retrieve additional entries, call 
<b>NetQueryDisplayInformation</b> again with the <i>Index</i> parameter set to the value returned in the <b>next_index</b> member of the last entry in <i>SortedBuffer</i>. Note that you should not use the value of the <b>next_index</b> member for any purpose except to retrieve more data with additional calls to 
<b>NetQueryDisplayInformation</b>.

</td>
</tr>
</table>
 




## -remarks



If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="https://msdn.microsoft.com/32f2ec06-822f-4d1e-bf51-5ae1d7355e60">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="security.pre_windows_2000_compatible_access_group">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="https://msdn.microsoft.com/846a5b81-d5bf-4275-a898-38e6ba308b8f">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="https://msdn.microsoft.com/fd3b718a-5eff-4894-9fc6-d157ddb67330">Access Control Model</a>.

The <b>NetQueryDisplayInformation</b> function only returns information to which the caller has Read access. The caller must have List Contents access to the Domain object, and  Enumerate Entire SAM Domain access on the SAM Server object  located in the System container.

The 
<b>NetQueryDisplayInformation</b> and 
<a href="https://msdn.microsoft.com/c56b3cf9-e0a2-4b66-a518-70753b79214c">NetGetDisplayInformationIndex</a> functions provide an efficient mechanism for enumerating user and group accounts. When possible, use these functions instead of the 
<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a> function or the 
<a href="https://msdn.microsoft.com/3f8fabce-94cb-41f5-9af1-04585ac3f16e">NetGroupEnum</a> function.

To enumerate trusting domains or member computer accounts, call 
<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a>, specifying the appropriate filter value to obtain the account information you require. To enumerate trusted domains, call the 
<a href="https://msdn.microsoft.com/5c371d5a-26cf-4a99-a8e1-006b6b3cc91f">LsaEnumerateTrustedDomains</a> or <a href="https://msdn.microsoft.com/4a203bff-c3e1-4d95-b556-617dc8c2e8c2">LsaEnumerateTrustedDomainsEx</a> function.

The number of entries returned by this function depends on the security descriptor located on the root domain object. The API will return  either the first 100 entries or the entire set of entries in the domain, depending on the access privileges of the user. The ACE used to control this behavior is "SAM-Enumerate-Entire-Domain", and is granted to Authenticated Users by default. Administrators can modify this setting to allow users to enumerate the entire domain.

Each call to 
<b>NetQueryDisplayInformation</b> returns a maximum of 100 objects. Calling the 
<b>NetQueryDisplayInformation</b> function to enumerate domain account information can be costly in terms of performance. If you are programming for Active Directory, you may be able to use methods on the 
<a href="https://msdn.microsoft.com/e8989795-8f72-476a-a69e-c0e8800289ab">IDirectorySearch</a> interface to make paged queries against the domain. For more information, see 
<a href="https://msdn.microsoft.com/1c5b3f72-6165-41ad-99d4-d68bc12ac10b">IDirectorySearch::SetSearchPreference</a> and 
<a href="https://msdn.microsoft.com/7514b372-1a7a-4a42-a814-af70a727c477">IDirectorySearch::ExecuteSearch</a>. To enumerate trusted domains, call the 
<a href="https://msdn.microsoft.com/4a203bff-c3e1-4d95-b556-617dc8c2e8c2">LsaEnumerateTrustedDomainsEx</a> function.


#### Examples

The following code sample demonstrates how to return group account information using a call to the 
<b>NetQueryDisplayInformation</b> function. If the user specifies a server name, the sample first calls the 
<a href="https://msdn.microsoft.com/a117fdfe-b52b-466f-9300-6455e91ea2a8">MultiByteToWideChar</a> function to convert the name to Unicode. The sample calls 
<b>NetQueryDisplayInformation</b>, specifying information level 3 (<a href="https://msdn.microsoft.com/8e467f20-2cfb-40ae-a8b2-a5350d736eed">NET_DISPLAY_GROUP</a>) to retrieve group account information. If there are entries to return, the sample returns the data and prints the group information. Finally, the code sample frees the memory allocated for the information buffer.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>#ifndef UNICODE
#define UNICODE
#endif

#include &lt;windows.h&gt;
#include &lt;stdio.h&gt;
#include &lt;lm.h&gt;

#pragma comment(lib, "netapi32.lib")

void main( int argc, char *argv[ ] )
{
   PNET_DISPLAY_GROUP pBuff, p;
   DWORD res, dwRec, i = 0;
   //
   // You can pass a NULL or empty string
   //  to retrieve the local information.
   //
   TCHAR szServer[255]=TEXT(""); 

   if(argc &gt; 1) 
      //
      // Check to see if a server name was passed;
      //  if so, convert it to Unicode.
      //
      MultiByteToWideChar(CP_ACP, 0, argv[1], -1, szServer, 255); 

   do // begin do
   { 
      //
      // Call the NetQueryDisplayInformation function;
      //   specify information level 3 (group account information).
      //
      res = NetQueryDisplayInformation(szServer, 3, i, 1000, MAX_PREFERRED_LENGTH, &amp;dwRec, (PVOID*) &amp;pBuff);
      //
      // If the call succeeds,
      //
      if((res==ERROR_SUCCESS) || (res==ERROR_MORE_DATA))
      {
         p = pBuff;
         for(;dwRec&gt;0;dwRec--)
         {
            //
            // Print the retrieved group information.
            //
            printf("Name:      %S\n"
                  "Comment:   %S\n"
                  "Group ID:  %u\n"
                  "Attributes: %u\n"
                  "--------------------------------\n",
                  p-&gt;grpi3_name,
                  p-&gt;grpi3_comment,
                  p-&gt;grpi3_group_id,
                  p-&gt;grpi3_attributes);
            //
            // If there is more data, set the index.
            //
            i = p-&gt;grpi3_next_index;
            p++;
         }
         //
         // Free the allocated memory.
         //
         NetApiBufferFree(pBuff);
      }
      else
         printf("Error: %u\n", res);
   //
   // Continue while there is more data.
   //
   } while (res==ERROR_MORE_DATA); // end do
   return;
}
</pre>
</td>
</tr>
</table></span></div>



## -see-also




<a href="https://msdn.microsoft.com/9c97420d-bc8a-42c9-b7ea-3d2ebc0034b3">Get Functions</a>



<a href="https://msdn.microsoft.com/5c371d5a-26cf-4a99-a8e1-006b6b3cc91f">LsaEnumerateTrustedDomains</a>



<a href="https://msdn.microsoft.com/4a203bff-c3e1-4d95-b556-617dc8c2e8c2">LsaEnumerateTrustedDomainsEx</a>



<a href="https://msdn.microsoft.com/8e467f20-2cfb-40ae-a8b2-a5350d736eed">NET_DISPLAY_GROUP</a>



<a href="https://msdn.microsoft.com/bdb1bef0-51f1-41d7-97fb-bda4ad24e386">NET_DISPLAY_MACHINE</a>



<a href="https://msdn.microsoft.com/308966f7-448c-4748-bbe7-9ac63afae1d9">NET_DISPLAY_USER</a>



<a href="https://msdn.microsoft.com/c56b3cf9-e0a2-4b66-a518-70753b79214c">NetGetDisplayInformationIndex</a>



<a href="https://msdn.microsoft.com/3f8fabce-94cb-41f5-9af1-04585ac3f16e">NetGroupEnum</a>



<a href="https://msdn.microsoft.com/b26ef3c0-934a-4840-8c06-4eaff5c9ff86">NetUserEnum</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

