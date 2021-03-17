---
UID: NF:lmaccess.NetQueryDisplayInformation
title: NetQueryDisplayInformation function (lmaccess.h)
description: The NetQueryDisplayInformation function returns user account, computer, or group account information. Call this function to quickly enumerate account information for display in user interfaces.
helpviewer_keywords: ["1","2","3","NetQueryDisplayInformation","NetQueryDisplayInformation function [Network Management]","_win32_netquerydisplayinformation","lmaccess/NetQueryDisplayInformation","netmgmt.netquerydisplayinformation"]
old-location: netmgmt\netquerydisplayinformation.htm
tech.root: NetMgmt
ms.assetid: 049f1ea3-4d23-4b35-8b08-7256859aed45
ms.date: 12/05/2018
ms.keywords: 1, 2, 3, NetQueryDisplayInformation, NetQueryDisplayInformation function [Network Management], _win32_netquerydisplayinformation, lmaccess/NetQueryDisplayInformation, netmgmt.netquerydisplayinformation
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetQueryDisplayInformation
 - lmaccess/NetQueryDisplayInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetQueryDisplayInformation
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
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_display_user">NET_DISPLAY_USER</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="2"></a><dl>
<dt><b>2</b></dt>
</dl>
</td>
<td width="60%">
Return individual computer information. The <i>SortedBuffer</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_display_machine">NET_DISPLAY_MACHINE</a> structures.

</td>
</tr>
<tr>
<td width="40%"><a id="3"></a><dl>
<dt><b>3</b></dt>
</dl>
</td>
<td width="60%">
Return group account information. The <i>SortedBuffer</i> parameter points to an array of 
<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_display_group">NET_DISPLAY_GROUP</a> structures.

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
<a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function. Note that you must free the buffer even if the function fails with ERROR_MORE_DATA. For more information, see the following Return Values section, and the topics 
<a href="/windows/desktop/NetMgmt/network-management-function-buffers">Network Management Function Buffers</a> and 
<a href="/windows/desktop/NetMgmt/network-management-function-buffer-lengths">Network Management Function Buffer Lengths</a>.

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

If you call this function on a domain controller that is running Active Directory, access is allowed or denied based on the access control list (ACL) for the <a href="/windows/desktop/SecAuthZ/securable-objects">securable object</a>. The default ACL permits all authenticated users and members of the "<a href="/windows/desktop/SecAuthZ/allowing-anonymous-access">Pre-Windows 2000 compatible access</a>" group to view the information. If you call this function on a member server or workstation, all authenticated users can view the information. For  information about anonymous access and restricting anonymous access on these platforms, see 
<a href="/windows/desktop/NetMgmt/security-requirements-for-the-network-management-functions">Security Requirements for the Network Management Functions</a>. For more information on ACLs, ACEs, and access tokens, see 
<a href="/windows/desktop/SecAuthZ/access-control-model">Access Control Model</a>.

The <b>NetQueryDisplayInformation</b> function only returns information to which the caller has Read access. The caller must have List Contents access to the Domain object, and  Enumerate Entire SAM Domain access on the SAM Server object  located in the System container.

The 
<b>NetQueryDisplayInformation</b> and 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetdisplayinformationindex">NetGetDisplayInformationIndex</a> functions provide an efficient mechanism for enumerating user and group accounts. When possible, use these functions instead of the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a> function or the 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupenum">NetGroupEnum</a> function.

To enumerate trusting domains or member computer accounts, call 
<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>, specifying the appropriate filter value to obtain the account information you require. To enumerate trusted domains, call the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains">LsaEnumerateTrustedDomains</a> or <a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex">LsaEnumerateTrustedDomainsEx</a> function.

The number of entries returned by this function depends on the security descriptor located on the root domain object. The API will return  either the first 100 entries or the entire set of entries in the domain, depending on the access privileges of the user. The ACE used to control this behavior is "SAM-Enumerate-Entire-Domain", and is granted to Authenticated Users by default. Administrators can modify this setting to allow users to enumerate the entire domain.

Each call to 
<b>NetQueryDisplayInformation</b> returns a maximum of 100 objects. Calling the 
<b>NetQueryDisplayInformation</b> function to enumerate domain account information can be costly in terms of performance. If you are programming for Active Directory, you may be able to use methods on the 
<a href="/windows/desktop/api/iads/nn-iads-idirectorysearch">IDirectorySearch</a> interface to make paged queries against the domain. For more information, see 
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-setsearchpreference">IDirectorySearch::SetSearchPreference</a> and 
<a href="/windows/desktop/api/iads/nf-iads-idirectorysearch-executesearch">IDirectorySearch::ExecuteSearch</a>. To enumerate trusted domains, call the 
<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex">LsaEnumerateTrustedDomainsEx</a> function.


#### Examples

The following code sample demonstrates how to return group account information using a call to the 
<b>NetQueryDisplayInformation</b> function. If the user specifies a server name, the sample first calls the 
<a href="/windows/desktop/api/stringapiset/nf-stringapiset-multibytetowidechar">MultiByteToWideChar</a> function to convert the name to Unicode. The sample calls 
<b>NetQueryDisplayInformation</b>, specifying information level 3 (<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_display_group">NET_DISPLAY_GROUP</a>) to retrieve group account information. If there are entries to return, the sample returns the data and prints the group information. Finally, the code sample frees the memory allocated for the information buffer.


```cpp
#ifndef UNICODE
#define UNICODE
#endif

#include <windows.h>
#include <stdio.h>
#include <lm.h>

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

   if(argc > 1) 
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
      res = NetQueryDisplayInformation(szServer, 3, i, 1000, MAX_PREFERRED_LENGTH, &dwRec, (PVOID*) &pBuff);
      //
      // If the call succeeds,
      //
      if((res==ERROR_SUCCESS) || (res==ERROR_MORE_DATA))
      {
         p = pBuff;
         for(;dwRec>0;dwRec--)
         {
            //
            // Print the retrieved group information.
            //
            printf("Name:      %S\n"
                  "Comment:   %S\n"
                  "Group ID:  %u\n"
                  "Attributes: %u\n"
                  "--------------------------------\n",
                  p->grpi3_name,
                  p->grpi3_comment,
                  p->grpi3_group_id,
                  p->grpi3_attributes);
            //
            // If there is more data, set the index.
            //
            i = p->grpi3_next_index;
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

```

## -see-also

<a href="/windows/desktop/NetMgmt/get-functions">Get Functions</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomains">LsaEnumerateTrustedDomains</a>



<a href="/windows/desktop/api/ntsecapi/nf-ntsecapi-lsaenumeratetrusteddomainsex">LsaEnumerateTrustedDomainsEx</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_display_group">NET_DISPLAY_GROUP</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_display_machine">NET_DISPLAY_MACHINE</a>



<a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_display_user">NET_DISPLAY_USER</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgetdisplayinformationindex">NetGetDisplayInformationIndex</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netgroupenum">NetGroupEnum</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netuserenum">NetUserEnum</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>